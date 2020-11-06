---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584796"
---
# <span data-ttu-id="03145-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="03145-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="03145-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03145-102">SYNOPSIS</span></span>
<span data-ttu-id="03145-103">Hämtar egenskaperna för en disk.</span><span class="sxs-lookup"><span data-stu-id="03145-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03145-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03145-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03145-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03145-105">DESCRIPTION</span></span>
<span data-ttu-id="03145-106">Cmdleten **Get-AzureRmDisk** hämtar egenskaperna för en disk.</span><span class="sxs-lookup"><span data-stu-id="03145-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="03145-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03145-107">EXAMPLES</span></span>

### <span data-ttu-id="03145-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03145-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="03145-109">Det här kommandot får egenskaperna för disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="03145-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="03145-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="03145-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="03145-111">Det här kommandot får egenskaperna för alla diskar i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="03145-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="03145-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="03145-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="03145-113">Det här kommandot får egenskaperna för alla diskar under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="03145-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="03145-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03145-114">PARAMETERS</span></span>

### <span data-ttu-id="03145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03145-115">-DefaultProfile</span></span>
<span data-ttu-id="03145-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03145-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03145-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="03145-117">-DiskName</span></span>
<span data-ttu-id="03145-118">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="03145-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03145-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03145-119">-ResourceGroupName</span></span>
<span data-ttu-id="03145-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="03145-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03145-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03145-121">CommonParameters</span></span>
<span data-ttu-id="03145-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03145-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03145-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03145-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03145-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03145-124">INPUTS</span></span>

### <span data-ttu-id="03145-125">System. String</span><span class="sxs-lookup"><span data-stu-id="03145-125">System.String</span></span>

## <span data-ttu-id="03145-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03145-126">OUTPUTS</span></span>

### <span data-ttu-id="03145-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="03145-127">System.Object</span></span>

## <span data-ttu-id="03145-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03145-128">NOTES</span></span>

## <span data-ttu-id="03145-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03145-129">RELATED LINKS</span></span>

