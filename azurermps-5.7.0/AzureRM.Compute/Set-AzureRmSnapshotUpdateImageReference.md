---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574342"
---
# <span data-ttu-id="82db1-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="82db1-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="82db1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82db1-102">SYNOPSIS</span></span>
<span data-ttu-id="82db1-103">Ställer in bild referens egenskaperna för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="82db1-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82db1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82db1-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82db1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82db1-105">DESCRIPTION</span></span>
<span data-ttu-id="82db1-106">Cmdleten **set-AzureRmSnapshotUpdateImageReference** anger bild referens egenskaperna för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="82db1-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="82db1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82db1-107">EXAMPLES</span></span>

### <span data-ttu-id="82db1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82db1-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="82db1-109">Med det första kommandot skapas ett lokalt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="82db1-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="82db1-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="82db1-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="82db1-111">Det andra kommandot anger det bild-ID och den logiska enhetens nummer 0 för ögonblicks bildens uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="82db1-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="82db1-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="82db1-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="82db1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82db1-113">PARAMETERS</span></span>

### <span data-ttu-id="82db1-114">-ID</span><span class="sxs-lookup"><span data-stu-id="82db1-114">-Id</span></span>
<span data-ttu-id="82db1-115">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="82db1-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="82db1-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="82db1-116">-Lun</span></span>
<span data-ttu-id="82db1-117">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="82db1-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82db1-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="82db1-118">-SnapshotUpdate</span></span>
<span data-ttu-id="82db1-119">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="82db1-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82db1-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82db1-120">-Confirm</span></span>
<span data-ttu-id="82db1-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82db1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82db1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82db1-122">-WhatIf</span></span>
<span data-ttu-id="82db1-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82db1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82db1-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82db1-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82db1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82db1-125">CommonParameters</span></span>
<span data-ttu-id="82db1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82db1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82db1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82db1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82db1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82db1-128">INPUTS</span></span>

### <span data-ttu-id="82db1-129">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="82db1-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="82db1-130">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="82db1-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="82db1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82db1-131">OUTPUTS</span></span>

### <span data-ttu-id="82db1-132">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="82db1-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="82db1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82db1-133">NOTES</span></span>

## <span data-ttu-id="82db1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82db1-134">RELATED LINKS</span></span>

