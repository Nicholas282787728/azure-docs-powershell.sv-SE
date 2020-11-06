---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578316"
---
# <span data-ttu-id="35286-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="35286-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="35286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35286-102">SYNOPSIS</span></span>
<span data-ttu-id="35286-103">Hämtar egenskaperna för en disk.</span><span class="sxs-lookup"><span data-stu-id="35286-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35286-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="35286-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35286-105">DESCRIPTION</span></span>
<span data-ttu-id="35286-106">Cmdleten **Get-AzureRmDisk** hämtar egenskaperna för en disk.</span><span class="sxs-lookup"><span data-stu-id="35286-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="35286-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35286-107">EXAMPLES</span></span>

### <span data-ttu-id="35286-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35286-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="35286-109">Det här kommandot får egenskaperna för disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="35286-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="35286-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="35286-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="35286-111">Det här kommandot får egenskaperna för alla diskar i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="35286-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="35286-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="35286-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="35286-113">Det här kommandot får egenskaperna för alla diskar under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="35286-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="35286-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35286-114">PARAMETERS</span></span>

### <span data-ttu-id="35286-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="35286-115">-DiskName</span></span>
<span data-ttu-id="35286-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="35286-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35286-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35286-117">-ResourceGroupName</span></span>
<span data-ttu-id="35286-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="35286-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35286-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35286-119">CommonParameters</span></span>
<span data-ttu-id="35286-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35286-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35286-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35286-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35286-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35286-122">INPUTS</span></span>

### <span data-ttu-id="35286-123">System. String</span><span class="sxs-lookup"><span data-stu-id="35286-123">System.String</span></span>

## <span data-ttu-id="35286-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35286-124">OUTPUTS</span></span>

### <span data-ttu-id="35286-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="35286-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="35286-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35286-126">NOTES</span></span>

## <span data-ttu-id="35286-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35286-127">RELATED LINKS</span></span>

