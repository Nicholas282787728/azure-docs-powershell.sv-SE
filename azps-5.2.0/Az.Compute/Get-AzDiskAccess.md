---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394491"
---
# <span data-ttu-id="1625d-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1625d-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="1625d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1625d-102">SYNOPSIS</span></span>
<span data-ttu-id="1625d-103">Hämtar egenskaper för disk åtkomst</span><span class="sxs-lookup"><span data-stu-id="1625d-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="1625d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1625d-104">SYNTAX</span></span>

### <span data-ttu-id="1625d-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1625d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1625d-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="1625d-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1625d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1625d-107">DESCRIPTION</span></span>
<span data-ttu-id="1625d-108">Cmdleten **Get-AzDiskAccess** hämtar egenskaperna för disk åtkomst</span><span class="sxs-lookup"><span data-stu-id="1625d-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="1625d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1625d-109">EXAMPLES</span></span>

### <span data-ttu-id="1625d-110">Exempel 1: använda standard parameter uppsättning</span><span class="sxs-lookup"><span data-stu-id="1625d-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="1625d-111">Det här kommandot får egenskaperna för en disk åtkomst resurs med namnet "DiskAccess01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1625d-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1625d-112">Exempel 2: Get-AzDiskAccess efter resurs grupp</span><span class="sxs-lookup"><span data-stu-id="1625d-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="1625d-113">Det här kommandot får egenskaperna för alla disk åtkomster i resurs gruppen ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="1625d-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="1625d-114">Exempel 3: få all åtkomst till diskar</span><span class="sxs-lookup"><span data-stu-id="1625d-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="1625d-115">Det här kommandot får egenskaperna för alla disk åtkomster under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1625d-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="1625d-116">Exempel 4: Hämta all disk åtkomst med jokertecken</span><span class="sxs-lookup"><span data-stu-id="1625d-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="1625d-117">Det här kommandot får egenskaperna för alla disk åtkomster under prenumerations namnet från och med ' DiskAccessMicrosoft '.</span><span class="sxs-lookup"><span data-stu-id="1625d-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="1625d-118">Exempel 5: få disk åtkomst med ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1625d-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="1625d-119">Det här kommandot får egenskaperna för en disk åtkomst med angiven ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1625d-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="1625d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1625d-120">PARAMETERS</span></span>

### <span data-ttu-id="1625d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1625d-121">-DefaultProfile</span></span>
<span data-ttu-id="1625d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1625d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1625d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1625d-123">-Name</span></span>
<span data-ttu-id="1625d-124">Anger namnet på en disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1625d-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1625d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1625d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1625d-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1625d-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1625d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1625d-127">-ResourceId</span></span>
<span data-ttu-id="1625d-128">Resurs-ID för disk åtkomst.</span><span class="sxs-lookup"><span data-stu-id="1625d-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1625d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1625d-129">CommonParameters</span></span>
<span data-ttu-id="1625d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1625d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1625d-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1625d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1625d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1625d-132">INPUTS</span></span>

### <span data-ttu-id="1625d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1625d-133">System.String</span></span>

## <span data-ttu-id="1625d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1625d-134">OUTPUTS</span></span>

### <span data-ttu-id="1625d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1625d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="1625d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1625d-136">NOTES</span></span>

## <span data-ttu-id="1625d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1625d-137">RELATED LINKS</span></span>
