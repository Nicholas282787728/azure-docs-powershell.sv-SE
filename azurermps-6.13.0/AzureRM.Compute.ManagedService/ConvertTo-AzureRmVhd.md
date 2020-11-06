---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574007"
---
# <span data-ttu-id="104ad-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="104ad-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="104ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="104ad-102">SYNOPSIS</span></span>
<span data-ttu-id="104ad-103">Konvertera virtuella hård diskar med Azure-stöd för Hyper-V VM till</span><span class="sxs-lookup"><span data-stu-id="104ad-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="104ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="104ad-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="104ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="104ad-105">DESCRIPTION</span></span>
<span data-ttu-id="104ad-106">Konvertera virtuella hård diskar med Azure-stöd för Hyper-V VM till</span><span class="sxs-lookup"><span data-stu-id="104ad-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="104ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="104ad-107">EXAMPLES</span></span>

### <span data-ttu-id="104ad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="104ad-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="104ad-109">Konvertera Hyper-V VM med namnet "test" till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="104ad-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="104ad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="104ad-110">PARAMETERS</span></span>

### <span data-ttu-id="104ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="104ad-111">-AsJob</span></span>
<span data-ttu-id="104ad-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="104ad-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="104ad-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="104ad-113">-ExportPath</span></span>
<span data-ttu-id="104ad-114">Sökvägen till export-mappen som innehåller filerna.</span><span class="sxs-lookup"><span data-stu-id="104ad-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="104ad-115">-Force</span></span>
<span data-ttu-id="104ad-116">Tvinga alternativet Exportera även om befintlig mapp hittas.</span><span class="sxs-lookup"><span data-stu-id="104ad-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="104ad-117">-HyperVServer</span></span>
<span data-ttu-id="104ad-118">DNS-namnet för Hyper-V-servern med "localhost" som standardvärde.</span><span class="sxs-lookup"><span data-stu-id="104ad-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="104ad-119">-HyperVVMName</span></span>
<span data-ttu-id="104ad-120">Namn på Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="104ad-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="104ad-121">-Confirm</span></span>
<span data-ttu-id="104ad-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="104ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="104ad-123">-WhatIf</span></span>
<span data-ttu-id="104ad-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="104ad-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="104ad-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="104ad-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="104ad-126">CommonParameters</span></span>
<span data-ttu-id="104ad-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="104ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="104ad-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="104ad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="104ad-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="104ad-129">INPUTS</span></span>

### <span data-ttu-id="104ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="104ad-130">System.String</span></span>

## <span data-ttu-id="104ad-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="104ad-131">OUTPUTS</span></span>

### <span data-ttu-id="104ad-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="104ad-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="104ad-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="104ad-133">NOTES</span></span>

## <span data-ttu-id="104ad-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="104ad-134">RELATED LINKS</span></span>
