---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745175"
---
# <span data-ttu-id="699ae-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="699ae-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="699ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="699ae-102">SYNOPSIS</span></span>
<span data-ttu-id="699ae-103">Hämtar inställningarna för tillägget diagnostik på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="699ae-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="699ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="699ae-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="699ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="699ae-105">DESCRIPTION</span></span>
<span data-ttu-id="699ae-106">Cmdleten **Get-AzVMDiagnosticsExtension** hämtar inställningarna för Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="699ae-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="699ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="699ae-107">EXAMPLES</span></span>

### <span data-ttu-id="699ae-108">Exempel 1: få tillägget installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="699ae-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="699ae-109">Det här kommandot får tillägget installerat på den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="699ae-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="699ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="699ae-110">PARAMETERS</span></span>

### <span data-ttu-id="699ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699ae-111">-DefaultProfile</span></span>
<span data-ttu-id="699ae-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="699ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ae-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="699ae-113">-Name</span></span>
<span data-ttu-id="699ae-114">Anger namnet på den diagnostiska anknytning som denna cmdlet hämtar inställningar för.</span><span class="sxs-lookup"><span data-stu-id="699ae-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="699ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="699ae-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="699ae-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="699ae-117">-Status</span><span class="sxs-lookup"><span data-stu-id="699ae-117">-Status</span></span>
<span data-ttu-id="699ae-118">Anger att denna cmdlet använder statusvärdet.</span><span class="sxs-lookup"><span data-stu-id="699ae-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="699ae-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="699ae-119">-VMName</span></span>
<span data-ttu-id="699ae-120">Anger namnet på den virtuella dator från vilken denna cmdlet får tillägget.</span><span class="sxs-lookup"><span data-stu-id="699ae-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="699ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ae-121">CommonParameters</span></span>
<span data-ttu-id="699ae-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ae-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="699ae-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ae-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="699ae-124">INPUTS</span></span>

### <span data-ttu-id="699ae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="699ae-125">System.String</span></span>

### <span data-ttu-id="699ae-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="699ae-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="699ae-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="699ae-127">OUTPUTS</span></span>

### <span data-ttu-id="699ae-128">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="699ae-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="699ae-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="699ae-129">NOTES</span></span>

## <span data-ttu-id="699ae-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="699ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="699ae-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="699ae-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="699ae-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="699ae-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


