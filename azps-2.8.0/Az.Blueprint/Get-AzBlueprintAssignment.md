---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745367"
---
# <span data-ttu-id="3f756-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3f756-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="3f756-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f756-102">SYNOPSIS</span></span>
<span data-ttu-id="3f756-103">Få en eller flera skisser.</span><span class="sxs-lookup"><span data-stu-id="3f756-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="3f756-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f756-104">SYNTAX</span></span>

### <span data-ttu-id="3f756-105">BlueprintAssignmentsBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="3f756-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f756-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="3f756-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f756-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f756-107">DESCRIPTION</span></span>
<span data-ttu-id="3f756-108">Få en eller flera skisser.</span><span class="sxs-lookup"><span data-stu-id="3f756-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="3f756-109">Skissa uppgifter finns i abonnemangs omfattningen.</span><span class="sxs-lookup"><span data-stu-id="3f756-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="3f756-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f756-110">EXAMPLES</span></span>

### <span data-ttu-id="3f756-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f756-111">Example 1</span></span>
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

<span data-ttu-id="3f756-112">Få skisserna i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3f756-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="3f756-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f756-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="3f756-114">Få skiss tilldelningen med det angivna namnet inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3f756-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="3f756-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f756-115">PARAMETERS</span></span>

### <span data-ttu-id="3f756-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f756-116">-DefaultProfile</span></span>
<span data-ttu-id="3f756-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f756-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f756-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f756-118">-Name</span></span>
<span data-ttu-id="3f756-119">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3f756-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f756-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f756-120">-SubscriptionId</span></span>
<span data-ttu-id="3f756-121">Abonnemangs-ID som skiss uppgiften distribueras till.</span><span class="sxs-lookup"><span data-stu-id="3f756-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f756-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f756-122">CommonParameters</span></span>
<span data-ttu-id="3f756-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f756-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f756-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f756-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f756-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f756-125">INPUTS</span></span>

### <span data-ttu-id="3f756-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3f756-126">System.String</span></span>

## <span data-ttu-id="3f756-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f756-127">OUTPUTS</span></span>

### <span data-ttu-id="3f756-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="3f756-128">System.Object</span></span>
## <span data-ttu-id="3f756-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f756-129">NOTES</span></span>

## <span data-ttu-id="3f756-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f756-130">RELATED LINKS</span></span>
