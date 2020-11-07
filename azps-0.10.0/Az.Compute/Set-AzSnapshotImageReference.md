---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 87786196e027597dc532bcaab2adfec4aa8c3892
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924861"
---
# <span data-ttu-id="02f00-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="02f00-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="02f00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02f00-102">SYNOPSIS</span></span>
<span data-ttu-id="02f00-103">Ställer in bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="02f00-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="02f00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02f00-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f00-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02f00-105">DESCRIPTION</span></span>
<span data-ttu-id="02f00-106">Cmdleten **set-AzSnapshotImageReference** anger bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="02f00-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="02f00-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02f00-107">EXAMPLES</span></span>

### <span data-ttu-id="02f00-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02f00-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="02f00-109">Det första kommandot skapar ett lokalt SnapShot-objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="02f00-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="02f00-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="02f00-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="02f00-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för ögonblicks bild obejct.</span><span class="sxs-lookup"><span data-stu-id="02f00-111">The second command sets the image ID and the logical unit number 0 for the snapshot obejct.</span></span>
<span data-ttu-id="02f00-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="02f00-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="02f00-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02f00-113">PARAMETERS</span></span>

### <span data-ttu-id="02f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f00-114">-DefaultProfile</span></span>
<span data-ttu-id="02f00-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02f00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f00-116">-ID</span><span class="sxs-lookup"><span data-stu-id="02f00-116">-Id</span></span>
<span data-ttu-id="02f00-117">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="02f00-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="02f00-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="02f00-118">-Lun</span></span>
<span data-ttu-id="02f00-119">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="02f00-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="02f00-120">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="02f00-120">-Snapshot</span></span>
<span data-ttu-id="02f00-121">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="02f00-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02f00-122">-Confirm</span></span>
<span data-ttu-id="02f00-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02f00-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f00-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f00-124">-WhatIf</span></span>
<span data-ttu-id="02f00-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02f00-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02f00-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02f00-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f00-127">CommonParameters</span></span>
<span data-ttu-id="02f00-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f00-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f00-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f00-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02f00-130">INPUTS</span></span>

### <span data-ttu-id="02f00-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="02f00-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="02f00-132">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="02f00-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="02f00-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02f00-133">OUTPUTS</span></span>

### <span data-ttu-id="02f00-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="02f00-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="02f00-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02f00-135">NOTES</span></span>

## <span data-ttu-id="02f00-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02f00-136">RELATED LINKS</span></span>

