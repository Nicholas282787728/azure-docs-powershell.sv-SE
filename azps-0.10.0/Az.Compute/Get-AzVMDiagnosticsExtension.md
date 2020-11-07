---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925198"
---
# <span data-ttu-id="3fa51-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa51-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3fa51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fa51-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa51-103">Hämtar inställningarna för tillägget diagnostik på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3fa51-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="3fa51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fa51-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fa51-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa51-106">Cmdleten **Get-AzVMDiagnosticsExtension** hämtar inställningarna för Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3fa51-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="3fa51-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fa51-107">EXAMPLES</span></span>

### <span data-ttu-id="3fa51-108">Exempel 1: få tillägget installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="3fa51-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="3fa51-109">Det här kommandot får tillägget installerat på den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="3fa51-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="3fa51-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fa51-110">PARAMETERS</span></span>

### <span data-ttu-id="3fa51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa51-111">-DefaultProfile</span></span>
<span data-ttu-id="3fa51-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa51-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fa51-113">-Name</span></span>
<span data-ttu-id="3fa51-114">Anger namnet på den diagnostiska anknytning som denna cmdlet hämtar inställningar för.</span><span class="sxs-lookup"><span data-stu-id="3fa51-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="3fa51-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa51-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fa51-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3fa51-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3fa51-117">-Status</span><span class="sxs-lookup"><span data-stu-id="3fa51-117">-Status</span></span>
<span data-ttu-id="3fa51-118">Anger att denna cmdlet använder statusvärdet.</span><span class="sxs-lookup"><span data-stu-id="3fa51-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa51-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="3fa51-119">-VMName</span></span>
<span data-ttu-id="3fa51-120">Anger namnet på den virtuella dator från vilken denna cmdlet får tillägget.</span><span class="sxs-lookup"><span data-stu-id="3fa51-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="3fa51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa51-121">CommonParameters</span></span>
<span data-ttu-id="3fa51-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa51-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa51-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa51-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fa51-124">INPUTS</span></span>

### <span data-ttu-id="3fa51-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="3fa51-125">None</span></span>
<span data-ttu-id="3fa51-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3fa51-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fa51-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fa51-127">OUTPUTS</span></span>

### <span data-ttu-id="3fa51-128">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3fa51-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3fa51-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fa51-129">NOTES</span></span>

## <span data-ttu-id="3fa51-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fa51-130">RELATED LINKS</span></span>

[<span data-ttu-id="3fa51-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa51-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3fa51-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3fa51-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


