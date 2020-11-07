---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925241"
---
# <span data-ttu-id="69fc4-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="69fc4-101">Get-AzDisk</span></span>

## <span data-ttu-id="69fc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="69fc4-103">Hämtar egenskaperna för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="69fc4-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="69fc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69fc4-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69fc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="69fc4-106">Cmdleten **Get-AzDisk** hämtar egenskaperna för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="69fc4-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="69fc4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="69fc4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69fc4-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="69fc4-109">Det här kommandot får egenskaperna för disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="69fc4-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="69fc4-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="69fc4-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="69fc4-111">Det här kommandot får egenskaperna för alla diskar i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="69fc4-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="69fc4-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="69fc4-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="69fc4-113">Det här kommandot får egenskaperna för alla diskar under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="69fc4-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="69fc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69fc4-114">PARAMETERS</span></span>

### <span data-ttu-id="69fc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fc4-115">-DefaultProfile</span></span>
<span data-ttu-id="69fc4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69fc4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fc4-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="69fc4-117">-DiskName</span></span>
<span data-ttu-id="69fc4-118">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="69fc4-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="69fc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="69fc4-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="69fc4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="69fc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fc4-121">CommonParameters</span></span>
<span data-ttu-id="69fc4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69fc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fc4-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fc4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fc4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69fc4-124">INPUTS</span></span>

### <span data-ttu-id="69fc4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="69fc4-125">System.String</span></span>

## <span data-ttu-id="69fc4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69fc4-126">OUTPUTS</span></span>

### <span data-ttu-id="69fc4-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="69fc4-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="69fc4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69fc4-128">NOTES</span></span>

## <span data-ttu-id="69fc4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69fc4-129">RELATED LINKS</span></span>

