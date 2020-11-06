---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575727"
---
# <span data-ttu-id="69077-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="69077-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="69077-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69077-102">SYNOPSIS</span></span>
<span data-ttu-id="69077-103">Konvertera virtuella hård diskar med Azure-stöd för Hyper-V VM till</span><span class="sxs-lookup"><span data-stu-id="69077-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69077-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69077-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="69077-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69077-105">DESCRIPTION</span></span>
<span data-ttu-id="69077-106">Konvertera virtuella hård diskar med Azure-stöd för Hyper-V VM till</span><span class="sxs-lookup"><span data-stu-id="69077-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="69077-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69077-107">EXAMPLES</span></span>

### <span data-ttu-id="69077-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69077-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="69077-109">Konvertera Hyper-V VM med namnet "test" till den aktuella mappen.</span><span class="sxs-lookup"><span data-stu-id="69077-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="69077-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69077-110">PARAMETERS</span></span>

### <span data-ttu-id="69077-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69077-111">-AsJob</span></span>
<span data-ttu-id="69077-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="69077-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69077-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="69077-113">-ExportPath</span></span>
<span data-ttu-id="69077-114">Sökvägen till export-mappen som innehåller filerna.</span><span class="sxs-lookup"><span data-stu-id="69077-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69077-115">-Force</span><span class="sxs-lookup"><span data-stu-id="69077-115">-Force</span></span>
<span data-ttu-id="69077-116">Tvinga alternativet Exportera även om befintlig mapp hittas.</span><span class="sxs-lookup"><span data-stu-id="69077-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69077-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="69077-117">-HyperVServer</span></span>
<span data-ttu-id="69077-118">DNS-namnet för Hyper-V-servern med "localhost" som standardvärde.</span><span class="sxs-lookup"><span data-stu-id="69077-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69077-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="69077-119">-HyperVVMName</span></span>
<span data-ttu-id="69077-120">Namn på Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="69077-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69077-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69077-121">CommonParameters</span></span>
<span data-ttu-id="69077-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69077-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69077-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69077-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69077-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69077-124">INPUTS</span></span>

### <span data-ttu-id="69077-125">System. String</span><span class="sxs-lookup"><span data-stu-id="69077-125">System.String</span></span>

## <span data-ttu-id="69077-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69077-126">OUTPUTS</span></span>

### <span data-ttu-id="69077-127">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="69077-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="69077-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69077-128">NOTES</span></span>

## <span data-ttu-id="69077-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69077-129">RELATED LINKS</span></span>

