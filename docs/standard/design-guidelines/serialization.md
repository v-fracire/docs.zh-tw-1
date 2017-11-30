---
title: Serialization1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: bebb27ac-9712-4196-9931-de19fc04dbac
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e63428400a7868b71a2d8e52637e4b22e4c44ee7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="serialization"></a><span data-ttu-id="b03bb-102">序列化</span><span class="sxs-lookup"><span data-stu-id="b03bb-102">Serialization</span></span>
<span data-ttu-id="b03bb-103">序列化是將物件轉換成可以輕易地保存或傳輸之格式的程序。</span><span class="sxs-lookup"><span data-stu-id="b03bb-103">Serialization is the process of converting an object into a format that can be readily persisted or transported.</span></span> <span data-ttu-id="b03bb-104">例如，您可以將物件序列化、 傳輸透過網際網路使用 HTTP，並還原序列化該目的地電腦上。</span><span class="sxs-lookup"><span data-stu-id="b03bb-104">For example, you can serialize an object, transport it over the Internet using HTTP, and deserialized it at the destination machine.</span></span>  
  
 <span data-ttu-id="b03bb-105">.NET Framework 提供三種主要的序列化技術，適用於各種序列化案例。</span><span class="sxs-lookup"><span data-stu-id="b03bb-105">The .NET Framework offers three main serialization technologies optimized for various serialization scenarios.</span></span> <span data-ttu-id="b03bb-106">下表列出這些技術以及與這些技術相關的主要 Framework 型別。</span><span class="sxs-lookup"><span data-stu-id="b03bb-106">The following table lists these technologies and the main Framework types related to these technologies.</span></span>  
  
|<span data-ttu-id="b03bb-107">**技術名稱**</span><span class="sxs-lookup"><span data-stu-id="b03bb-107">**Technology Name**</span></span>|<span data-ttu-id="b03bb-108">**主要類型**</span><span class="sxs-lookup"><span data-stu-id="b03bb-108">**Main Types**</span></span>|<span data-ttu-id="b03bb-109">**案例**</span><span class="sxs-lookup"><span data-stu-id="b03bb-109">**Scenarios**</span></span>|  
|-------------------------|--------------------|-------------------|  
|<span data-ttu-id="b03bb-110">**資料合約序列化**</span><span class="sxs-lookup"><span data-stu-id="b03bb-110">**Data Contract Serialization**</span></span>|<xref:System.Runtime.Serialization.DataContractAttribute> <br /> <xref:System.Runtime.Serialization.DataMemberAttribute> <br /> <xref:System.Runtime.Serialization.DataContractSerializer> <br /> <xref:System.Runtime.Serialization.NetDataContractSerializer> <br /> <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> <br /> <xref:System.Runtime.Serialization.ISerializable>|<span data-ttu-id="b03bb-111">一般持續性</span><span class="sxs-lookup"><span data-stu-id="b03bb-111">General persistence</span></span><br /><span data-ttu-id="b03bb-112">Web 服務</span><span class="sxs-lookup"><span data-stu-id="b03bb-112">Web Services</span></span><br /><span data-ttu-id="b03bb-113">JSON</span><span class="sxs-lookup"><span data-stu-id="b03bb-113">JSON</span></span>|  
|<span data-ttu-id="b03bb-114">**XML 序列化**</span><span class="sxs-lookup"><span data-stu-id="b03bb-114">**XML Serialization**</span></span>|<xref:System.Xml.Serialization.XmlSerializer>|<span data-ttu-id="b03bb-115">XML 格式的 XML 外觀的完整控制權</span><span class="sxs-lookup"><span data-stu-id="b03bb-115">XML format with full control over the shape of the XML</span></span>|  
|<span data-ttu-id="b03bb-116">**執行階段序列化 （二進位檔和 SOAP）**</span><span class="sxs-lookup"><span data-stu-id="b03bb-116">**Runtime Serialization (Binary and SOAP)**</span></span>|<xref:System.SerializableAttribute> <br /> <xref:System.Runtime.Serialization.ISerializable> <br /> <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> <br /> <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter>|<span data-ttu-id="b03bb-117">.NET 遠端處理</span><span class="sxs-lookup"><span data-stu-id="b03bb-117">.NET Remoting</span></span>|  
  
 <span data-ttu-id="b03bb-118">**✓ 不要**考慮序列化，當您設計新的類型。</span><span class="sxs-lookup"><span data-stu-id="b03bb-118">**✓ DO** think about serialization when you design new types.</span></span>  
  
## <a name="choosing-the-right-serialization-technology-to-support"></a><span data-ttu-id="b03bb-119">選擇要支援的正確序列化技術</span><span class="sxs-lookup"><span data-stu-id="b03bb-119">Choosing the Right Serialization Technology to Support</span></span>  
 <span data-ttu-id="b03bb-120">**✓ 考慮**支援資料合約序列化，如果您的型別執行個體可能需要保存或用於 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="b03bb-120">**✓ CONSIDER** supporting Data Contract Serialization if instances of your type might need to be persisted or used in Web Services.</span></span>  
  
 <span data-ttu-id="b03bb-121">**✓ 考慮**支援之 XML 序列化，而不是，或除了資料合約序列化，如果您需要更充分掌控型別序列化時所產生的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="b03bb-121">**✓ CONSIDER** supporting the XML Serialization instead of or in addition to Data Contract Serialization if you need more control over the XML format that is produced when the type is serialized.</span></span>  
  
 <span data-ttu-id="b03bb-122">這可能需要一些不支援資料合約序列化，比方說，若要產生的 XML 屬性的互通性案例中，您需要使用 XML 建構中。</span><span class="sxs-lookup"><span data-stu-id="b03bb-122">This may be necessary in some interoperability scenarios where you need to use an XML construct that is not supported by Data Contract Serialization, for example, to produce XML attributes.</span></span>  
  
 <span data-ttu-id="b03bb-123">**✓ 考慮**支援執行階段序列化，如果需要行經.NET 遠端處理界限類型執行個體。</span><span class="sxs-lookup"><span data-stu-id="b03bb-123">**✓ CONSIDER** supporting the Runtime Serialization if instances of your type need to travel across .NET Remoting boundaries.</span></span>  
  
 <span data-ttu-id="b03bb-124">**請避免 x**支援執行階段序列化或 XML 序列化，只會針對一般的持續性的原因。</span><span class="sxs-lookup"><span data-stu-id="b03bb-124">**X AVOID** supporting Runtime Serialization or XML Serialization just for general persistence reasons.</span></span> <span data-ttu-id="b03bb-125">偏好改為使用資料合約序列化。</span><span class="sxs-lookup"><span data-stu-id="b03bb-125">Prefer Data Contract Serialization instead.</span></span>  
  
## <a name="supporting-data-contract-serialization"></a><span data-ttu-id="b03bb-126">支援資料合約序列化</span><span class="sxs-lookup"><span data-stu-id="b03bb-126">Supporting Data Contract Serialization</span></span>  
 <span data-ttu-id="b03bb-127">型別可以藉由套用支援資料合約序列化<xref:System.Runtime.Serialization.DataContractAttribute>型別和<xref:System.Runtime.Serialization.DataMemberAttribute>類型成員 （欄位和屬性）。</span><span class="sxs-lookup"><span data-stu-id="b03bb-127">Types can support Data Contract Serialization by applying the <xref:System.Runtime.Serialization.DataContractAttribute> to the type and the <xref:System.Runtime.Serialization.DataMemberAttribute> to the members (fields and properties) of the type.</span></span>  
  
 <span data-ttu-id="b03bb-128">**✓ 考慮**標示的型別公開的資料成員，如果型別可以用在部分信任中。</span><span class="sxs-lookup"><span data-stu-id="b03bb-128">**✓ CONSIDER** marking data members of your type public if the type can be used in partial trust.</span></span>  
  
 <span data-ttu-id="b03bb-129">在完全信任，資料合約序列化程式可以序列化和還原序列化非公用類型和成員，但只有公用成員可以序列化，並且在部分信任中還原序列化。</span><span class="sxs-lookup"><span data-stu-id="b03bb-129">In full trust, Data Contract serializers can serialize and deserialize nonpublic types and members, but only public members can be serialized and deserialized in partial trust.</span></span>  
  
 <span data-ttu-id="b03bb-130">**✓ 不要**實作上擁有的所有屬性的 getter 和 setter <xref:System.Runtime.Serialization.DataMemberAttribute>。</span><span class="sxs-lookup"><span data-stu-id="b03bb-130">**✓ DO** implement a getter and setter on all properties that have <xref:System.Runtime.Serialization.DataMemberAttribute>.</span></span> <span data-ttu-id="b03bb-131">資料合約序列化程式會要求 getter 和 setter，才會被視為可序列化類型。</span><span class="sxs-lookup"><span data-stu-id="b03bb-131">Data Contract serializers require both the getter and the setter for the type to be considered serializable.</span></span> <span data-ttu-id="b03bb-132">（在.NET Framework 3.5 SP1，有些集合屬性可以是僅。）如果此型別不會在部分信任中使用，則其中一個或兩個屬性存取子可以不是 public。</span><span class="sxs-lookup"><span data-stu-id="b03bb-132">(In .NET Framework 3.5 SP1, some collection properties can be get-only.) If the type won’t be used in partial trust, one or both of the property accessors can be nonpublic.</span></span>  
  
 <span data-ttu-id="b03bb-133">**✓ 考慮**序列化回呼使用已還原序列化的執行個體的初始設定。</span><span class="sxs-lookup"><span data-stu-id="b03bb-133">**✓ CONSIDER** using the serialization callbacks for initialization of deserialized instances.</span></span>  
  
 <span data-ttu-id="b03bb-134">當還原序列化物件時，不會呼叫建構函式。</span><span class="sxs-lookup"><span data-stu-id="b03bb-134">Constructors are not called when objects are deserialized.</span></span> <span data-ttu-id="b03bb-135">（沒有規則的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b03bb-135">(There are exceptions to the rule.</span></span> <span data-ttu-id="b03bb-136">建構函式的集合標記為<xref:System.Runtime.Serialization.CollectionDataContractAttribute>會還原序列化期間呼叫。)因此，任何標準建構期間執行的邏輯必須實作為其中一個序列化回呼。</span><span class="sxs-lookup"><span data-stu-id="b03bb-136">Constructors of collections marked with <xref:System.Runtime.Serialization.CollectionDataContractAttribute> are called during deserialization.) Therefore, any logic that executes during normal construction needs to be implemented as one of the serialization callbacks.</span></span>  
  
 <span data-ttu-id="b03bb-137">`OnDeserializedAttribute`是最常使用的回呼屬性。</span><span class="sxs-lookup"><span data-stu-id="b03bb-137">`OnDeserializedAttribute` is the most commonly used callback attribute.</span></span> <span data-ttu-id="b03bb-138">此系列中的其他屬性為 <xref:System.Runtime.Serialization.OnDeserializingAttribute>、<xref:System.Runtime.Serialization.OnSerializingAttribute> 和 <xref:System.Runtime.Serialization.OnSerializedAttribute>。</span><span class="sxs-lookup"><span data-stu-id="b03bb-138">The other attributes in the family are <xref:System.Runtime.Serialization.OnDeserializingAttribute>,  <xref:System.Runtime.Serialization.OnSerializingAttribute>, and <xref:System.Runtime.Serialization.OnSerializedAttribute>.</span></span> <span data-ttu-id="b03bb-139">這些屬性可用來分別標記在還原序列化之前、序列化之前以及最後在序列化之後所執行的回呼。</span><span class="sxs-lookup"><span data-stu-id="b03bb-139">They can be used to mark callbacks that get executed before deserialization, before serialization, and finally, after serialization, respectively.</span></span>  
  
 <span data-ttu-id="b03bb-140">**✓ 考慮**使用<xref:System.Runtime.Serialization.KnownTypeAttribute>表示還原序列化複雜物件圖形時，應使用的具象類型。</span><span class="sxs-lookup"><span data-stu-id="b03bb-140">**✓ CONSIDER** using the <xref:System.Runtime.Serialization.KnownTypeAttribute> to indicate concrete types that should be used when deserializing a complex object graph.</span></span>  
  
 <span data-ttu-id="b03bb-141">**✓ 不要**考慮向後和向前相容性時建立或變更可序列化型別。</span><span class="sxs-lookup"><span data-stu-id="b03bb-141">**✓ DO** consider backward and forward compatibility when creating or changing serializable types.</span></span>  
  
 <span data-ttu-id="b03bb-142">請牢記，型別之未來版本的序列化資料流可以還原序列化成該型別的目前版本，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b03bb-142">Keep in mind that serialized streams of future versions of your type can be deserialized into the current version of the type, and vice versa.</span></span>  
  
 <span data-ttu-id="b03bb-143">請確定您了解，資料成員，即使私用和內部的無法變更其名稱、 類型或即使它們在未來版本的型別中的順序除非特別注意會被保留合約使用明確的參數，對資料合約屬性.</span><span class="sxs-lookup"><span data-stu-id="b03bb-143">Make sure you understand that data members, even private and internal, cannot change their names, types, or even their order in future versions of the type unless special care is taken to preserve the contract using explicit parameters to the data contract attributes.</span></span>  
  
 <span data-ttu-id="b03bb-144">變更可序列化型別時，請測試相容性的序列化。</span><span class="sxs-lookup"><span data-stu-id="b03bb-144">Test compatibility of serialization when making changes to serializable types.</span></span> <span data-ttu-id="b03bb-145">請嘗試將新的版本還原序列化成舊的版本，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b03bb-145">Try deserializing the new version into an old version, and vice versa.</span></span>  
  
 <span data-ttu-id="b03bb-146">**✓ 考慮**實作<xref:System.Runtime.Serialization.IExtensibleDataObject>允許之類型的不同版本之間的往返。</span><span class="sxs-lookup"><span data-stu-id="b03bb-146">**✓ CONSIDER** implementing <xref:System.Runtime.Serialization.IExtensibleDataObject> to allow round-tripping between different versions of the type.</span></span>  
  
 <span data-ttu-id="b03bb-147">此介面可讓序列化程式確保往返期間不會有任何資料遺失。</span><span class="sxs-lookup"><span data-stu-id="b03bb-147">The interface allows the serializer to ensure that no data is lost during round-tripping.</span></span> <span data-ttu-id="b03bb-148"><xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType>屬性用來儲存任何資料，從未來版本的最新版本，無法辨識的型別，因此它不能將它儲存在其資料成員。</span><span class="sxs-lookup"><span data-stu-id="b03bb-148">The <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType> property is used to store any data from the future version of the type that is unknown to the current version, and so it cannot store it in its data members.</span></span> <span data-ttu-id="b03bb-149">當目前的版本是後續序列化和還原序列化到未來的版本時，其他資料可序列化資料流中使用。</span><span class="sxs-lookup"><span data-stu-id="b03bb-149">When the current version is subsequently serialized and deserialized into a future version, the additional data will be available in the serialized stream.</span></span>  
  
## <a name="supporting-xml-serialization"></a><span data-ttu-id="b03bb-150">支援 XML 序列化</span><span class="sxs-lookup"><span data-stu-id="b03bb-150">Supporting XML Serialization</span></span>  
 <span data-ttu-id="b03bb-151">資料合約序列化即為主要 （預設值） 的序列化技術，在.NET Framework 中，但是有資料合約序列化不支援的序列化情況。</span><span class="sxs-lookup"><span data-stu-id="b03bb-151">Data Contract Serialization is the main (default) serialization technology in the .NET Framework, but there are serialization scenarios that Data Contract Serialization does not support.</span></span> <span data-ttu-id="b03bb-152">例如，它無法讓您完全控制序列化程式所產生或使用之 XML 的形狀。</span><span class="sxs-lookup"><span data-stu-id="b03bb-152">For example, it does not give you full control over the shape of XML produced or consumed by the serializer.</span></span> <span data-ttu-id="b03bb-153">如果需要這類良好的控制，XML 序列化必須使用，而且您必須設計您的型別支援這種序列化技術。</span><span class="sxs-lookup"><span data-stu-id="b03bb-153">If such fine control is required, XML Serialization has to be used, and you need to design your types to support this serialization technology.</span></span>  
  
 <span data-ttu-id="b03bb-154">**請避免 x**專為 XML 序列化，設計您的型別，除非您有非常強大的理由，來控制 XML 的外觀產生。</span><span class="sxs-lookup"><span data-stu-id="b03bb-154">**X AVOID** designing your types specifically for XML Serialization, unless you have a very strong reason to control the shape of the XML produced.</span></span> <span data-ttu-id="b03bb-155">這項序列化技術已經由前一節所討論的資料合約序列化所取代。</span><span class="sxs-lookup"><span data-stu-id="b03bb-155">This serialization technology has been superseded by the Data Contract Serialization discussed in the previous section.</span></span>  
  
 <span data-ttu-id="b03bb-156">**✓ 考慮**實作<xref:System.Xml.Serialization.IXmlSerializable>介面，如果您想要比藉由套用 XML 序列化屬性提供的哪些序列化的 XML 外觀的更多控制權。</span><span class="sxs-lookup"><span data-stu-id="b03bb-156">**✓ CONSIDER** implementing the <xref:System.Xml.Serialization.IXmlSerializable> interface if you want even more control over the shape of the serialized XML than what’s offered by applying the XML Serialization attributes.</span></span> <span data-ttu-id="b03bb-157">兩個介面方法<xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A>和<xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>，讓您完整控制序列化的 XML 資料流。</span><span class="sxs-lookup"><span data-stu-id="b03bb-157">Two methods of the interface, <xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> and <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>, allow you to fully control the serialized XML stream.</span></span> <span data-ttu-id="b03bb-158">您也可以控制所套用的類型取得產生的 XML 結構描述`XmlSchemaProviderAttribute`。</span><span class="sxs-lookup"><span data-stu-id="b03bb-158">You can also control the XML schema that gets generated for the type by applying the `XmlSchemaProviderAttribute`.</span></span>  
  
## <a name="supporting-runtime-serialization"></a><span data-ttu-id="b03bb-159">支援執行階段序列化</span><span class="sxs-lookup"><span data-stu-id="b03bb-159">Supporting Runtime Serialization</span></span>  
 <span data-ttu-id="b03bb-160">執行階段序列化是由.NET 遠端處理的技術。</span><span class="sxs-lookup"><span data-stu-id="b03bb-160">Runtime Serialization is a technology used by .NET Remoting.</span></span> <span data-ttu-id="b03bb-161">如果您認為您的型別會使用.NET 遠端處理傳輸，您需要確定它們支援執行階段序列化。</span><span class="sxs-lookup"><span data-stu-id="b03bb-161">If you think your types will be transported using .NET Remoting, you need to make sure they support Runtime Serialization.</span></span>  
  
 <span data-ttu-id="b03bb-162">可提供執行階段序列化的基本支援，請套用<xref:System.SerializableAttribute>，而且更進階的案例涉及實作簡單的執行階段序列化模式 (實作<xref:System.Runtime.Serialization.ISerializable>並提供序列化建構函式)。</span><span class="sxs-lookup"><span data-stu-id="b03bb-162">The basic support for Runtime Serialization can be provided by applying the <xref:System.SerializableAttribute>, and more advanced scenarios involve implementing a simple Runtime Serializable Pattern (implement <xref:System.Runtime.Serialization.ISerializable> and provide serialization constructor).</span></span>  
  
 <span data-ttu-id="b03bb-163">**✓ 考慮**支援執行階段序列化，如果您的型別會使用與.NET 遠端處理。</span><span class="sxs-lookup"><span data-stu-id="b03bb-163">**✓ CONSIDER** supporting Runtime Serialization if your types will be used with .NET Remoting.</span></span> <span data-ttu-id="b03bb-164">例如，<xref:System.AddIn?displayProperty=nameWithType>命名空間會使用.NET 遠端處理，並讓所有的型別之間交換`System.AddIn`增益集必須支援執行階段序列化。</span><span class="sxs-lookup"><span data-stu-id="b03bb-164">For example, the <xref:System.AddIn?displayProperty=nameWithType> namespace uses .NET Remoting, and so all types exchanged between `System.AddIn` add-ins need to support Runtime Serialization.</span></span>  
  
 <span data-ttu-id="b03bb-165">**✓ 考慮**實作的執行階段序列化模式，如果您想要完整控制序列化程序。</span><span class="sxs-lookup"><span data-stu-id="b03bb-165">**✓ CONSIDER** implementing the Runtime Serializable Pattern if you want complete control over the serialization process.</span></span> <span data-ttu-id="b03bb-166">例如，如果您想要在資料序列化或還原序列化時加以轉換。</span><span class="sxs-lookup"><span data-stu-id="b03bb-166">For example, if you want to transform data as it gets serialized or deserialized.</span></span>  
  
 <span data-ttu-id="b03bb-167">此模式非常簡單。</span><span class="sxs-lookup"><span data-stu-id="b03bb-167">The pattern is very simple.</span></span> <span data-ttu-id="b03bb-168">您只需要實作 <xref:System.Runtime.Serialization.ISerializable> 介面，並提供還原序列化物件時使用的特殊建構函式。</span><span class="sxs-lookup"><span data-stu-id="b03bb-168">All you need to do is implement the <xref:System.Runtime.Serialization.ISerializable> interface and provide a special constructor that is used when the object is deserialized.</span></span>  
  
 <span data-ttu-id="b03bb-169">**✓ 不要**進行保護序列化建構函式，並提供兩個參數類型和名為完全依照此處的範例所示。</span><span class="sxs-lookup"><span data-stu-id="b03bb-169">**✓ DO** make the serialization constructor protected and provide two parameters typed and named exactly as shown in the sample here.</span></span>  
  
```  
[Serializable]  
public class Person : ISerializable {  
    protected Person(SerializationInfo info, StreamingContext context) {  
        ...  
    }  
}  
```  
  
 <span data-ttu-id="b03bb-170">**✓ 不要**實作`ISerializable`成員明確。</span><span class="sxs-lookup"><span data-stu-id="b03bb-170">**✓ DO** implement the `ISerializable` members explicitly.</span></span>  
  
 <span data-ttu-id="b03bb-171">**✓ 不要**套用連結要求即可<xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType>實作。</span><span class="sxs-lookup"><span data-stu-id="b03bb-171">**✓ DO** apply a link demand to <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> implementation.</span></span> <span data-ttu-id="b03bb-172">這可確保只有完全信任的核心和執行階段序列化程式可以存取的成員。</span><span class="sxs-lookup"><span data-stu-id="b03bb-172">This ensures that only fully trusted core and the Runtime Serializer have access to the member.</span></span>  
  
 <span data-ttu-id="b03bb-173">*部分 © 2005年，2009 Microsoft Corporation。All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="b03bb-173">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="b03bb-174">*皮耳森教育，inc.從權限所印製[Framework 設計方針： 慣例、 慣用語和可重複使用.NET 程式庫，第 2 版的模式](http://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina 並 Brad Abrams，發行 2008 年 10 月 22 日由Addison Wesley Professional，做為 Microsoft Windows 程式開發系列的一部分。*</span><span class="sxs-lookup"><span data-stu-id="b03bb-174">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](http://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b03bb-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b03bb-175">See Also</span></span>  
 [<span data-ttu-id="b03bb-176">Framework 設計方針</span><span class="sxs-lookup"><span data-stu-id="b03bb-176">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
 [<span data-ttu-id="b03bb-177">使用指導方針</span><span class="sxs-lookup"><span data-stu-id="b03bb-177">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)