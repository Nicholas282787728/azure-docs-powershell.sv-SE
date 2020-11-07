---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 1cfa355de00a66690c4c6a01c45d9631db30ba6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917261"
---
# <span data-ttu-id="9bc6e-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="9bc6e-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="9bc6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bc6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc6e-103">Ställer in bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="9bc6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bc6e-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bc6e-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc6e-106">Cmdleten **set-AzSnapshotImageReference** anger bild referens egenskaperna för ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="9bc6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bc6e-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc6e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9bc6e-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="9bc6e-109">Det första kommandot skapar ett lokalt SnapShot-objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="9bc6e-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="9bc6e-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="9bc6e-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9bc6e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9bc6e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bc6e-113">PARAMETERS</span></span>

### <span data-ttu-id="9bc6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc6e-114">-DefaultProfile</span></span>
<span data-ttu-id="9bc6e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc6e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="9bc6e-116">-Id</span></span>
<span data-ttu-id="9bc6e-117">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="9bc6e-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="9bc6e-118">-Lun</span></span>
<span data-ttu-id="9bc6e-119">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="9bc6e-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="9bc6e-120">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="9bc6e-120">-Snapshot</span></span>
<span data-ttu-id="9bc6e-121">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="9bc6e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bc6e-122">-Confirm</span></span>
<span data-ttu-id="9bc6e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc6e-124">-WhatIf</span></span>
<span data-ttu-id="9bc6e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bc6e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc6e-127">CommonParameters</span></span>
<span data-ttu-id="9bc6e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc6e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc6e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc6e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bc6e-130">INPUTS</span></span>

### <span data-ttu-id="9bc6e-131">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="9bc6e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="9bc6e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9bc6e-132">System.String</span></span>

### <span data-ttu-id="9bc6e-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9bc6e-133">System.Int32</span></span>

## <span data-ttu-id="9bc6e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bc6e-134">OUTPUTS</span></span>

### <span data-ttu-id="9bc6e-135">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="9bc6e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="9bc6e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bc6e-136">NOTES</span></span>

## <span data-ttu-id="9bc6e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bc6e-137">RELATED LINKS</span></span>
