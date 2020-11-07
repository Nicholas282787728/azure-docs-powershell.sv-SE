---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755616"
---
# <span data-ttu-id="61c1f-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="61c1f-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="61c1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="61c1f-103">Hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61c1f-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61c1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61c1f-104">SYNTAX</span></span>

### <span data-ttu-id="61c1f-105">WindowsParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="61c1f-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="61c1f-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="61c1f-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="61c1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61c1f-107">DESCRIPTION</span></span>
<span data-ttu-id="61c1f-108">Cmdleten **Get-AzureRmVMBootDiagnosticsData** hämtar startdiagnostik-data för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61c1f-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="61c1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61c1f-109">EXAMPLES</span></span>

### <span data-ttu-id="61c1f-110">Exempel 1: Hämta data från startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="61c1f-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="61c1f-111">Det här kommandot får Boot Diagnostics-data för den virtuella datorn med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="61c1f-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="61c1f-112">Denna virtuella dator kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="61c1f-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="61c1f-113">Kommandot lagrar data i angiven lokal sökväg.</span><span class="sxs-lookup"><span data-stu-id="61c1f-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="61c1f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="61c1f-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="61c1f-115">-Linux</span></span>
<span data-ttu-id="61c1f-116">Anger att den virtuella datorn kör Linux-operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="61c1f-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c1f-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="61c1f-117">-LocalPath</span></span>
<span data-ttu-id="61c1f-118">Anger den lokala sökvägen för startdiagnostikens data.</span><span class="sxs-lookup"><span data-stu-id="61c1f-118">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c1f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="61c1f-119">-Name</span></span>
<span data-ttu-id="61c1f-120">Anger namnet på den virtuella dator för vilken denna cmdlet hämtar diagnostikdata.</span><span class="sxs-lookup"><span data-stu-id="61c1f-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="61c1f-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="61c1f-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61c1f-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="61c1f-123">-Windows</span></span>
<span data-ttu-id="61c1f-124">Anger att operativ systemet Windows körs på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="61c1f-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c1f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c1f-125">CommonParameters</span></span>
<span data-ttu-id="61c1f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c1f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c1f-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c1f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c1f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61c1f-128">INPUTS</span></span>

### <span data-ttu-id="61c1f-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="61c1f-129">None</span></span>
<span data-ttu-id="61c1f-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="61c1f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61c1f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61c1f-131">OUTPUTS</span></span>

## <span data-ttu-id="61c1f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61c1f-132">NOTES</span></span>

## <span data-ttu-id="61c1f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61c1f-133">RELATED LINKS</span></span>

[<span data-ttu-id="61c1f-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="61c1f-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


