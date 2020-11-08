---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089830"
---
# <span data-ttu-id="0f0a1-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f0a1-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="0f0a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0a1-103">Tar bort tillägget diagnostik från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="0f0a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f0a1-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f0a1-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0a1-106">Cmdleten **Remove-AzVMDiagnosticsExtension** tar bort ett Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="0f0a1-107">Du måste skicka utdata från denna cmdlet till Update-AzVM cmdlet för att implementera ändringarna.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="0f0a1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f0a1-108">EXAMPLES</span></span>

### <span data-ttu-id="0f0a1-109">Exempel 1: ta bort tillägget diagnostik från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="0f0a1-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="0f0a1-110">Det här kommandot tar bort tillägget från en virtuell dator med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="0f0a1-111">Kommandot skickar resultatet till Update-AzVM cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f0a1-112">Det kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="0f0a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f0a1-113">PARAMETERS</span></span>

### <span data-ttu-id="0f0a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0a1-114">-DefaultProfile</span></span>
<span data-ttu-id="0f0a1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0a1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f0a1-116">-Name</span></span>
<span data-ttu-id="0f0a1-117">Anger namnet på den diagnostiska anknytning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f0a1-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0f0a1-118">-NoWait</span></span>
<span data-ttu-id="0f0a1-119">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0f0a1-120">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f0a1-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0f0a1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0f0a1-123">-VMName</span></span>
<span data-ttu-id="0f0a1-124">Anger namnet på den virtuella dator som cmdleten tar bort ett diagnostiktest från.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="0f0a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0a1-125">CommonParameters</span></span>
<span data-ttu-id="0f0a1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0a1-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f0a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0a1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f0a1-128">INPUTS</span></span>

### <span data-ttu-id="0f0a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0f0a1-129">System.String</span></span>

## <span data-ttu-id="0f0a1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f0a1-130">OUTPUTS</span></span>

### <span data-ttu-id="0f0a1-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0f0a1-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0f0a1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f0a1-132">NOTES</span></span>

## <span data-ttu-id="0f0a1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f0a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="0f0a1-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f0a1-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="0f0a1-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0f0a1-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="0f0a1-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0f0a1-136">Update-AzVM</span></span>](./Update-AzVM.md)

