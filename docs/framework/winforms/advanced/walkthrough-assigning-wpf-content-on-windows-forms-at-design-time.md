---
title: 逐步解說：在設計階段指派 Windows Forms 的 WPF 內容
ms.date: 03/30/2017
helpviewer_keywords:
- WPF content [Windows Forms], assigning at design time
- ElementHost control [Windows Forms], assigning WPF content at design time
- interoperability [WPF]
- Windows Forms, content assignments
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: b3e9ef93-7e0f-4a2f-8f1e-3437609a1eb7
ms.openlocfilehash: a2597348075f870723abb07d13ac7a687e47ab41
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2019
ms.locfileid: "56304397"
---
# <a name="walkthrough-assigning-wpf-content-on-windows-forms-at-design-time"></a>逐步解說：在設計階段指派 Windows Forms 的 WPF 內容
本逐步解說示範如何選取要在表單上顯示的 Windows Presentation Foundation (WPF) 控制項類型。 您可以選取包含在專案中的任何 WPF 控制項類型。

 在這個逐步解說中，您將執行下列工作：

-   建立專案。

-   建立 WPF 控制項類型。

-   選取 WPF 控制項。

> [!NOTE]
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [ **工具** ] 功能表中選取 [ **匯入和匯出設定** ]。 如需詳細資訊，請參閱[將 Visual Studio IDE 個人化](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
## <a name="prerequisites"></a>必要條件  
 您需要下列元件才能完成此逐步解說：  
  
-   Visual Studio 2012.  
  
## <a name="creating-the-project"></a>建立專案  
 第一個步驟是建立 Windows Form 專案。  
  
> [!NOTE]
>  裝載 WPF 內容時，只支援 C# 和 Visual Basic 專案。  
  
#### <a name="to-create-the-project"></a>若要建立專案  
  
-   建立新的 Windows Forms 應用程式專案在 Visual Basic 或 Visual C# 中名為`SelectingWpfContent`。  
  
## <a name="creating-the-wpf-control-types"></a>建立 WPF 控制項類型  
 當您將 WPF 控制項類型加入專案之後，即可在不同的 <xref:System.Windows.Forms.Integration.ElementHost> 控制項中裝載這些類型。  
  
#### <a name="to-create-wpf-control-types"></a>建立 WPF 控制項類型  
  
1.  將新的 WPF <xref:System.Windows.Controls.UserControl> 專案加入方案。 使用控制項類型的預設名稱 `UserControl1.xaml`。 如需詳細資訊，請參閱[逐步解說：在設計階段建立 Windows Form 上的新 WPF 內容](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)。  
  
2.  在 [設計] 檢視中，確定已選取 `UserControl1`。 如需詳細資訊，請參閱[如何：選取並移動設計介面上的項目](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100))。  
  
3.  在 **屬性**視窗中，設定的值<xref:System.Windows.FrameworkElement.Width%2A>並<xref:System.Windows.FrameworkElement.Height%2A>屬性，以`200`。  
  
4.  新增<xref:System.Windows.Controls.TextBox?displayProperty=nameWithType>若要控制<xref:System.Windows.Controls.UserControl>並將值<xref:System.Windows.Controls.TextBox.Text%2A>屬性設**裝載內容**。  
  
5.  將第二個 WPF <xref:System.Windows.Controls.UserControl> 加入專案。 使用控制項類型的預設名稱 `UserControl2.xaml`。  
  
6.  在 **屬性**視窗中，設定的值<xref:System.Windows.FrameworkElement.Width%2A>並<xref:System.Windows.FrameworkElement.Height%2A>屬性，以`200`。  
  
7.  新增<xref:System.Windows.Controls.TextBox?displayProperty=nameWithType>若要控制<xref:System.Windows.Controls.UserControl>並將值<xref:System.Windows.Controls.TextBox.Text%2A>屬性設**裝載的內容 2**。  
  
 **請注意**一般情況下，您應該裝載更複雜的 WPF 內容。 
  <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> 控制項在此僅供說明用途使用。  
  
1.  建置專案。  
  
## <a name="selecting-wpf-controls"></a>選取 WPF 控制項  
 您可以對已裝載內容的 <xref:System.Windows.Forms.Integration.ElementHost> 控制項，指派不同的 WPF 內容。  
  
#### <a name="to-select-wpf-controls"></a>選取 WPF 控制項  
  
1.  在 Windows Form 設計工具中開啟 `Form1`。  
  
2.  在 **工具箱**，按兩下`UserControl1`若要建立的執行個體`UserControl1`表單上。  
  
     
  `UserControl1` 的執行個體裝載於名為 `elementHost1` 的新 <xref:System.Windows.Forms.Integration.ElementHost> 控制項中。  
  
3.  中的智慧標籤面板`elementHost1`，開啟**選擇裝載內容**下拉式清單。  
  
4.  選取  **UserControl2**從下拉式清單方塊。  
  
     
  `elementHost1` 控制項現在會裝載 `UserControl2` 類型的執行個體。  
  
5.  在 [**屬性**] 視窗中，確認<xref:System.Windows.Forms.Integration.ElementHost.Child%2A>屬性設定為**UserControl2**。  
  
6.  從**工具箱**，請在**WPF 互通性**群組中，拖曳<xref:System.Windows.Forms.Integration.ElementHost>控制項拖曳至表單。  
  
     新控制項的預設名稱為 `elementHost2`。  
  
7.  中的智慧標籤面板`elementHost2`，開啟**選擇裝載內容**下拉式清單。  
  
8.  選取  **UserControl1**從下拉式清單。  
  
9. 
  `elementHost2` 控制項現在會裝載 `UserControl1` 類型的執行個體。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [移轉和互通性](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)
- [使用 WPF 控制項](../../../../docs/framework/winforms/advanced/using-wpf-controls.md)
- [在 Visual Studio 中設計 XAML](/visualstudio/designers/designing-xaml-in-visual-studio)
