---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576587"
---
# <span data-ttu-id="eb5fa-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb5fa-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="eb5fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5fa-103">Tar bort tillägget diagnostik från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb5fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb5fa-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb5fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5fa-106">Cmdleten **Remove-AzureRmVMDiagnosticsExtension** tar bort ett Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="eb5fa-107">Du måste skicka utdata från denna cmdlet till Update-AzureRmVM cmdlet för att implementera ändringarna.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="eb5fa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb5fa-108">EXAMPLES</span></span>

### <span data-ttu-id="eb5fa-109">Exempel 1: ta bort tillägget diagnostik från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="eb5fa-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="eb5fa-110">Det här kommandot tar bort tillägget från en virtuell dator med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="eb5fa-111">Kommandot skickar resultatet till Update-AzureRmVM cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb5fa-112">Det kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="eb5fa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb5fa-113">PARAMETERS</span></span>

### <span data-ttu-id="eb5fa-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb5fa-114">-Name</span></span>
<span data-ttu-id="eb5fa-115">Anger namnet på den diagnostiska anknytning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5fa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5fa-116">-ResourceGroupName</span></span>
<span data-ttu-id="eb5fa-117">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-117">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5fa-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb5fa-118">-VMName</span></span>
<span data-ttu-id="eb5fa-119">Anger namnet på den virtuella dator som cmdleten tar bort ett diagnostiktest från.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5fa-120">CommonParameters</span></span>
<span data-ttu-id="eb5fa-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5fa-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5fa-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb5fa-123">INPUTS</span></span>

### <span data-ttu-id="eb5fa-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="eb5fa-124">None</span></span>
<span data-ttu-id="eb5fa-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="eb5fa-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb5fa-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb5fa-126">OUTPUTS</span></span>

## <span data-ttu-id="eb5fa-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb5fa-127">NOTES</span></span>

## <span data-ttu-id="eb5fa-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb5fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb5fa-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb5fa-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="eb5fa-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb5fa-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="eb5fa-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eb5fa-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


