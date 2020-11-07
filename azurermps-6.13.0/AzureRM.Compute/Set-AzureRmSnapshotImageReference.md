---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: d650d60c1fdcdf8293bb612a471c1604df01eecf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755345"
---
# <span data-ttu-id="bc94f-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="bc94f-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="bc94f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc94f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc94f-103">Ställer in bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="bc94f-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc94f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc94f-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc94f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc94f-105">DESCRIPTION</span></span>
<span data-ttu-id="bc94f-106">Cmdleten **set-AzureRmSnapshotImageReference** anger bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="bc94f-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="bc94f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc94f-107">EXAMPLES</span></span>

### <span data-ttu-id="bc94f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bc94f-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="bc94f-109">Det första kommandot skapar ett lokalt SnapShot-objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="bc94f-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bc94f-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="bc94f-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="bc94f-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="bc94f-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="bc94f-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bc94f-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bc94f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc94f-113">PARAMETERS</span></span>

### <span data-ttu-id="bc94f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc94f-114">-DefaultProfile</span></span>
<span data-ttu-id="bc94f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc94f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc94f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="bc94f-116">-Id</span></span>
<span data-ttu-id="bc94f-117">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="bc94f-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="bc94f-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="bc94f-118">-Lun</span></span>
<span data-ttu-id="bc94f-119">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="bc94f-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc94f-120">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="bc94f-120">-Snapshot</span></span>
<span data-ttu-id="bc94f-121">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="bc94f-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc94f-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc94f-122">-Confirm</span></span>
<span data-ttu-id="bc94f-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc94f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc94f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc94f-124">-WhatIf</span></span>
<span data-ttu-id="bc94f-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc94f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc94f-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc94f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc94f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc94f-127">CommonParameters</span></span>
<span data-ttu-id="bc94f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc94f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc94f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc94f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc94f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc94f-130">INPUTS</span></span>

### <span data-ttu-id="bc94f-131">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="bc94f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="bc94f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bc94f-132">System.String</span></span>

### <span data-ttu-id="bc94f-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bc94f-133">System.Int32</span></span>

## <span data-ttu-id="bc94f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc94f-134">OUTPUTS</span></span>

### <span data-ttu-id="bc94f-135">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="bc94f-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="bc94f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc94f-136">NOTES</span></span>

## <span data-ttu-id="bc94f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc94f-137">RELATED LINKS</span></span>
