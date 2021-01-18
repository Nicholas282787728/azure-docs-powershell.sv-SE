---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524659"
---
# <span data-ttu-id="620e5-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="620e5-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="620e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="620e5-102">SYNOPSIS</span></span>
<span data-ttu-id="620e5-103">Få en eller flera skisser.</span><span class="sxs-lookup"><span data-stu-id="620e5-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="620e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="620e5-104">SYNTAX</span></span>

### <span data-ttu-id="620e5-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="620e5-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="620e5-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="620e5-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="620e5-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="620e5-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="620e5-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="620e5-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="620e5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="620e5-109">DESCRIPTION</span></span>
<span data-ttu-id="620e5-110">Få en eller flera skisser.</span><span class="sxs-lookup"><span data-stu-id="620e5-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="620e5-111">Skissa uppgifter finns i abonnemangs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="620e5-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="620e5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="620e5-112">EXAMPLES</span></span>

### <span data-ttu-id="620e5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="620e5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="620e5-114">Få skisserna i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="620e5-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="620e5-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="620e5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="620e5-116">Få skiss tilldelningen med det angivna namnet inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="620e5-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="620e5-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="620e5-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="620e5-118">Få skisserna i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="620e5-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="620e5-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="620e5-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="620e5-120">Få skiss tilldelningen med det angivna namnet i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="620e5-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="620e5-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="620e5-121">PARAMETERS</span></span>

### <span data-ttu-id="620e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620e5-122">-DefaultProfile</span></span>
<span data-ttu-id="620e5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="620e5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="620e5-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="620e5-124">-ManagementGroupId</span></span>
<span data-ttu-id="620e5-125">ID för hanterings gruppen där skiss tilldelningen har sparats.</span><span class="sxs-lookup"><span data-stu-id="620e5-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620e5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="620e5-126">-Name</span></span>
<span data-ttu-id="620e5-127">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="620e5-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620e5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="620e5-128">-SubscriptionId</span></span>
<span data-ttu-id="620e5-129">Abonnemangs-ID som skiss uppgiften distribueras till.</span><span class="sxs-lookup"><span data-stu-id="620e5-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620e5-130">CommonParameters</span></span>
<span data-ttu-id="620e5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620e5-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="620e5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620e5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="620e5-133">INPUTS</span></span>

### <span data-ttu-id="620e5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="620e5-134">System.String</span></span>

## <span data-ttu-id="620e5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="620e5-135">OUTPUTS</span></span>

### <span data-ttu-id="620e5-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="620e5-136">System.Object</span></span>
## <span data-ttu-id="620e5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="620e5-137">NOTES</span></span>

## <span data-ttu-id="620e5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="620e5-138">RELATED LINKS</span></span>
