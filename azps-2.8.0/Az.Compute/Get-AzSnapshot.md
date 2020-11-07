---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 534af1de5513520eeef02161916de6dce1655df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745186"
---
# <span data-ttu-id="8bb98-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bb98-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="8bb98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bb98-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb98-103">Hämtar egenskaperna för en ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="8bb98-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="8bb98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bb98-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bb98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bb98-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb98-106">Cmdleten **Get-AzSnapshot** hämtar egenskaperna för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="8bb98-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="8bb98-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bb98-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb98-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8bb98-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="8bb98-109">Det här kommandot får egenskaperna för alla stillbilder av abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8bb98-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="8bb98-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8bb98-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="8bb98-111">Det här kommandot får egenskaperna för alla stillbilder i resurs gruppen "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="8bb98-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="8bb98-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8bb98-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="8bb98-113">Det här kommandot får egenskaperna för fixeringen med namnet "SnapshotName1" i resurs gruppen med namnet "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="8bb98-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="8bb98-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="8bb98-114">Example 4</span></span>
```
PS C:\> Get-AzSnapshot -SnapshotName "SnapshotName*"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="8bb98-115">Det här kommandot får alla stillbilder som börjar med "SnapshotName"</span><span class="sxs-lookup"><span data-stu-id="8bb98-115">This command gets all snapshots that start with "SnapshotName"</span></span>

## <span data-ttu-id="8bb98-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bb98-116">PARAMETERS</span></span>

### <span data-ttu-id="8bb98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb98-117">-DefaultProfile</span></span>
<span data-ttu-id="8bb98-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb98-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb98-119">-ResourceGroupName</span></span>
<span data-ttu-id="8bb98-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8bb98-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8bb98-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="8bb98-121">-SnapshotName</span></span>
<span data-ttu-id="8bb98-122">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="8bb98-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8bb98-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb98-123">CommonParameters</span></span>
<span data-ttu-id="8bb98-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb98-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb98-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bb98-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb98-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bb98-126">INPUTS</span></span>

### <span data-ttu-id="8bb98-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb98-127">System.String</span></span>

## <span data-ttu-id="8bb98-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bb98-128">OUTPUTS</span></span>

### <span data-ttu-id="8bb98-129">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bb98-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8bb98-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bb98-130">NOTES</span></span>

## <span data-ttu-id="8bb98-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bb98-131">RELATED LINKS</span></span>
