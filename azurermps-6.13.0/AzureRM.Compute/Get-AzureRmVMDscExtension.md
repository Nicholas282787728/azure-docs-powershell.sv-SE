---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 6bab7e7bc823008d018d53f146aec54f599f63d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756689"
---
# <span data-ttu-id="a65be-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a65be-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="a65be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a65be-102">SYNOPSIS</span></span>
<span data-ttu-id="a65be-103">Hämtar inställningarna för DSC-tillägget på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a65be-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a65be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a65be-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a65be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a65be-105">DESCRIPTION</span></span>
<span data-ttu-id="a65be-106">Cmdleten **Get-AzureRmVMDscExtension** hämtar inställningarna för tillägget DSC (önskad State Configuration) på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a65be-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="a65be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a65be-107">EXAMPLES</span></span>

### <span data-ttu-id="a65be-108">Exempel 1: Hämta inställningar för en DSC-anknytning</span><span class="sxs-lookup"><span data-stu-id="a65be-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="a65be-109">Det här kommandot får inställningar för tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="a65be-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="a65be-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a65be-110">PARAMETERS</span></span>

### <span data-ttu-id="a65be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65be-111">-DefaultProfile</span></span>
<span data-ttu-id="a65be-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a65be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65be-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="a65be-113">-Name</span></span>
<span data-ttu-id="a65be-114">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="a65be-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a65be-115">Set-AzureRmVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, som är samma värde som används av **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="a65be-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="a65be-116">Ange endast den här parametern om du har ändrat standard namnet i cmdleten **set-AzureRmVMDscExtension** eller använt ett annat resurs namn i en resurs hanterares mall.</span><span class="sxs-lookup"><span data-stu-id="a65be-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65be-117">-ResourceGroupName</span></span>
<span data-ttu-id="a65be-118">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a65be-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65be-119">-Status</span><span class="sxs-lookup"><span data-stu-id="a65be-119">-Status</span></span>
<span data-ttu-id="a65be-120">Anger att denna cmdlet får instans vyn av DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="a65be-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65be-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="a65be-121">-VMName</span></span>
<span data-ttu-id="a65be-122">Anger namnet på en virtuell dator för vilken denna cmdlet får DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="a65be-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65be-123">CommonParameters</span></span>
<span data-ttu-id="a65be-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65be-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a65be-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65be-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a65be-126">INPUTS</span></span>

### <span data-ttu-id="a65be-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a65be-127">System.String</span></span>

### <span data-ttu-id="a65be-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a65be-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a65be-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a65be-129">OUTPUTS</span></span>

### <span data-ttu-id="a65be-130">Microsoft. Azure. commands. Compute. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a65be-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="a65be-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a65be-131">NOTES</span></span>

## <span data-ttu-id="a65be-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a65be-132">RELATED LINKS</span></span>

[<span data-ttu-id="a65be-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a65be-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="a65be-134">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a65be-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


