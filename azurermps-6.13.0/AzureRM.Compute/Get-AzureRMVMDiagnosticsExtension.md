---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fbc357decbf4bdcd2e378294fed43125d38fd873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575312"
---
# <span data-ttu-id="1d9ea-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1d9ea-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="1d9ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9ea-103">Hämtar inställningarna för tillägget diagnostik på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d9ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d9ea-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9ea-106">Cmdleten **Get-AzureRmVMDiagnosticsExtension** hämtar inställningarna för Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1d9ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d9ea-107">EXAMPLES</span></span>

### <span data-ttu-id="1d9ea-108">Exempel 1: få tillägget installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1d9ea-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="1d9ea-109">Det här kommandot får tillägget installerat på den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="1d9ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d9ea-110">PARAMETERS</span></span>

### <span data-ttu-id="1d9ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9ea-111">-DefaultProfile</span></span>
<span data-ttu-id="1d9ea-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9ea-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d9ea-113">-Name</span></span>
<span data-ttu-id="1d9ea-114">Anger namnet på den diagnostiska anknytning som denna cmdlet hämtar inställningar för.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d9ea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9ea-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d9ea-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1d9ea-117">-Status</span><span class="sxs-lookup"><span data-stu-id="1d9ea-117">-Status</span></span>
<span data-ttu-id="1d9ea-118">Anger att denna cmdlet använder statusvärdet.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d9ea-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d9ea-119">-VMName</span></span>
<span data-ttu-id="1d9ea-120">Anger namnet på den virtuella dator från vilken denna cmdlet får tillägget.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d9ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9ea-121">CommonParameters</span></span>
<span data-ttu-id="1d9ea-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9ea-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9ea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9ea-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d9ea-124">INPUTS</span></span>

### <span data-ttu-id="1d9ea-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9ea-125">System.String</span></span>

### <span data-ttu-id="1d9ea-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d9ea-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d9ea-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d9ea-127">OUTPUTS</span></span>

### <span data-ttu-id="1d9ea-128">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="1d9ea-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="1d9ea-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d9ea-129">NOTES</span></span>

## <span data-ttu-id="1d9ea-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d9ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="1d9ea-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1d9ea-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1d9ea-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1d9ea-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


