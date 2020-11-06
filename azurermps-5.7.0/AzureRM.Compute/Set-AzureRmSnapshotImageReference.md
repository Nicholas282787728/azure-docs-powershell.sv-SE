---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573524"
---
# <span data-ttu-id="ea890-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="ea890-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="ea890-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea890-102">SYNOPSIS</span></span>
<span data-ttu-id="ea890-103">Ställer in bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea890-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea890-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea890-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea890-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea890-105">DESCRIPTION</span></span>
<span data-ttu-id="ea890-106">Cmdleten **set-AzureRmSnapshotImageReference** anger bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea890-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="ea890-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea890-107">EXAMPLES</span></span>

### <span data-ttu-id="ea890-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea890-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="ea890-109">Det första kommandot skapar ett lokalt SnapShot-objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="ea890-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ea890-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="ea890-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ea890-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="ea890-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="ea890-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ea890-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ea890-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea890-113">PARAMETERS</span></span>

### <span data-ttu-id="ea890-114">-ID</span><span class="sxs-lookup"><span data-stu-id="ea890-114">-Id</span></span>
<span data-ttu-id="ea890-115">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="ea890-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="ea890-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="ea890-116">-Lun</span></span>
<span data-ttu-id="ea890-117">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="ea890-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="ea890-118">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="ea890-118">-Snapshot</span></span>
<span data-ttu-id="ea890-119">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea890-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea890-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea890-120">-Confirm</span></span>
<span data-ttu-id="ea890-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea890-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea890-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea890-122">-WhatIf</span></span>
<span data-ttu-id="ea890-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea890-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea890-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea890-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea890-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea890-125">CommonParameters</span></span>
<span data-ttu-id="ea890-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea890-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea890-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea890-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea890-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea890-128">INPUTS</span></span>

### <span data-ttu-id="ea890-129">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ea890-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="ea890-130">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ea890-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ea890-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea890-131">OUTPUTS</span></span>

### <span data-ttu-id="ea890-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="ea890-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="ea890-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea890-133">NOTES</span></span>

## <span data-ttu-id="ea890-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea890-134">RELATED LINKS</span></span>

