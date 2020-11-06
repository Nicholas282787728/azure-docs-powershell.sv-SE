---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577254"
---
# <span data-ttu-id="1eaf7-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1eaf7-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="1eaf7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1eaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaf7-103">Hämtar inställningarna för tillägget diagnostik på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eaf7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1eaf7-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="1eaf7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1eaf7-105">DESCRIPTION</span></span>
<span data-ttu-id="1eaf7-106">Cmdleten **Get-AzureRmVMDiagnosticsExtension** hämtar inställningarna för Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1eaf7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1eaf7-107">EXAMPLES</span></span>

### <span data-ttu-id="1eaf7-108">Exempel 1: få tillägget installerat på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1eaf7-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="1eaf7-109">Det här kommandot får tillägget installerat på den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="1eaf7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1eaf7-110">PARAMETERS</span></span>

### <span data-ttu-id="1eaf7-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="1eaf7-111">-Name</span></span>
<span data-ttu-id="1eaf7-112">Anger namnet på den diagnostiska anknytning som denna cmdlet hämtar inställningar för.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="1eaf7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaf7-113">-ResourceGroupName</span></span>
<span data-ttu-id="1eaf7-114">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1eaf7-115">-Status</span><span class="sxs-lookup"><span data-stu-id="1eaf7-115">-Status</span></span>
<span data-ttu-id="1eaf7-116">Anger att denna cmdlet använder statusvärdet.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="1eaf7-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="1eaf7-117">-VMName</span></span>
<span data-ttu-id="1eaf7-118">Anger namnet på den virtuella dator från vilken denna cmdlet får tillägget.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="1eaf7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eaf7-119">CommonParameters</span></span>
<span data-ttu-id="1eaf7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eaf7-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eaf7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eaf7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1eaf7-122">INPUTS</span></span>

### <span data-ttu-id="1eaf7-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="1eaf7-123">None</span></span>
<span data-ttu-id="1eaf7-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1eaf7-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1eaf7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1eaf7-125">OUTPUTS</span></span>

## <span data-ttu-id="1eaf7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1eaf7-126">NOTES</span></span>

## <span data-ttu-id="1eaf7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1eaf7-127">RELATED LINKS</span></span>

[<span data-ttu-id="1eaf7-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1eaf7-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1eaf7-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1eaf7-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


