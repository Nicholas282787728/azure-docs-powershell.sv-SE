---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924957"
---
# <span data-ttu-id="bd3c8-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bd3c8-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="bd3c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3c8-103">Tar bort tillägget diagnostik från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="bd3c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd3c8-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd3c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd3c8-105">DESCRIPTION</span></span>
<span data-ttu-id="bd3c8-106">Cmdleten **Remove-AzVMDiagnosticsExtension** tar bort ett Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="bd3c8-107">Du måste skicka utdata från denna cmdlet till Update-AzVM cmdlet för att implementera ändringarna.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="bd3c8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd3c8-108">EXAMPLES</span></span>

### <span data-ttu-id="bd3c8-109">Exempel 1: ta bort tillägget diagnostik från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="bd3c8-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="bd3c8-110">Det här kommandot tar bort tillägget från en virtuell dator med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="bd3c8-111">Kommandot skickar resultatet till Update-AzVM cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bd3c8-112">Det kommandot uppdaterar den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="bd3c8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd3c8-113">PARAMETERS</span></span>

### <span data-ttu-id="bd3c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd3c8-114">-DefaultProfile</span></span>
<span data-ttu-id="bd3c8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd3c8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd3c8-116">-Name</span></span>
<span data-ttu-id="bd3c8-117">Anger namnet på den diagnostiska anknytning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd3c8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd3c8-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd3c8-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bd3c8-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="bd3c8-120">-VMName</span></span>
<span data-ttu-id="bd3c8-121">Anger namnet på den virtuella dator som cmdleten tar bort ett diagnostiktest från.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="bd3c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3c8-122">CommonParameters</span></span>
<span data-ttu-id="bd3c8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3c8-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd3c8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3c8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd3c8-125">INPUTS</span></span>

### <span data-ttu-id="bd3c8-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="bd3c8-126">None</span></span>
<span data-ttu-id="bd3c8-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bd3c8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd3c8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd3c8-128">OUTPUTS</span></span>

### <span data-ttu-id="bd3c8-129">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bd3c8-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bd3c8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd3c8-130">NOTES</span></span>

## <span data-ttu-id="bd3c8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd3c8-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd3c8-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bd3c8-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="bd3c8-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bd3c8-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="bd3c8-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd3c8-134">Update-AzVM</span></span>](./Update-AzVM.md)


