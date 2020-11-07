---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930333"
---
# <span data-ttu-id="3ffc8-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ffc8-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3ffc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ffc8-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffc8-103">Tar bort tillägget diagnostik från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ffc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ffc8-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ffc8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ffc8-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffc8-106">Cmdleten **Remove-AzureRmVMDiagnosticsExtension** tar bort ett Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3ffc8-107">Du måste skicka utdata från denna cmdlet till Update-AzureRmVM cmdlet för att implementera ändringarna.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3ffc8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ffc8-108">EXAMPLES</span></span>

### <span data-ttu-id="3ffc8-109">Exempel 1: ta bort tillägget diagnostik från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="3ffc8-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="3ffc8-110">Det här kommandot tar bort tillägget från en virtuell dator med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3ffc8-111">Kommandot skickar resultatet till Update-AzureRmVM cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ffc8-112">Det kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3ffc8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ffc8-113">PARAMETERS</span></span>

### <span data-ttu-id="3ffc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffc8-114">-DefaultProfile</span></span>
<span data-ttu-id="3ffc8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffc8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ffc8-116">-Name</span></span>
<span data-ttu-id="3ffc8-117">Anger namnet på den diagnostiska anknytning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3ffc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ffc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="3ffc8-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3ffc8-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="3ffc8-120">-VMName</span></span>
<span data-ttu-id="3ffc8-121">Anger namnet på den virtuella dator som cmdleten tar bort ett diagnostiktest från.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="3ffc8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffc8-122">CommonParameters</span></span>
<span data-ttu-id="3ffc8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffc8-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffc8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffc8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ffc8-125">INPUTS</span></span>

### <span data-ttu-id="3ffc8-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ffc8-126">None</span></span>
<span data-ttu-id="3ffc8-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3ffc8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ffc8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ffc8-128">OUTPUTS</span></span>

### <span data-ttu-id="3ffc8-129">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3ffc8-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3ffc8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ffc8-130">NOTES</span></span>

## <span data-ttu-id="3ffc8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ffc8-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ffc8-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ffc8-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="3ffc8-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3ffc8-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="3ffc8-134">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3ffc8-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


