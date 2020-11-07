---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758125"
---
# <span data-ttu-id="b4cda-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="b4cda-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="b4cda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4cda-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cda-103">Anger bild referens egenskaperna för ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="b4cda-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4cda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4cda-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4cda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4cda-105">DESCRIPTION</span></span>
<span data-ttu-id="b4cda-106">Cmdleten **set-AzureRmDiskUpdateImageReference** anger bild referens egenskaperna för ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="b4cda-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="b4cda-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4cda-107">EXAMPLES</span></span>

### <span data-ttu-id="b4cda-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4cda-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="b4cda-109">Det första kommandot skapar ett uppdaterings objekt för lokala diskar med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b4cda-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b4cda-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="b4cda-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="b4cda-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="b4cda-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="b4cda-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b4cda-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b4cda-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4cda-113">PARAMETERS</span></span>

### <span data-ttu-id="b4cda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cda-114">-DefaultProfile</span></span>
<span data-ttu-id="b4cda-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4cda-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4cda-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b4cda-116">-DiskUpdate</span></span>
<span data-ttu-id="b4cda-117">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="b4cda-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cda-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b4cda-118">-Id</span></span>
<span data-ttu-id="b4cda-119">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="b4cda-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="b4cda-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="b4cda-120">-Lun</span></span>
<span data-ttu-id="b4cda-121">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="b4cda-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cda-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4cda-122">-Confirm</span></span>
<span data-ttu-id="b4cda-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4cda-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4cda-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cda-124">-WhatIf</span></span>
<span data-ttu-id="b4cda-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4cda-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4cda-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4cda-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4cda-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cda-127">CommonParameters</span></span>
<span data-ttu-id="b4cda-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4cda-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cda-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4cda-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cda-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4cda-130">INPUTS</span></span>

### <span data-ttu-id="b4cda-131">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b4cda-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="b4cda-132">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b4cda-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b4cda-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4cda-133">OUTPUTS</span></span>

### <span data-ttu-id="b4cda-134">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b4cda-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="b4cda-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4cda-135">NOTES</span></span>

## <span data-ttu-id="b4cda-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4cda-136">RELATED LINKS</span></span>

