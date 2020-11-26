---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270566"
---
# <span data-ttu-id="1ae86-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae86-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="1ae86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ae86-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae86-103">Hämtar en särskild registrerings definition eller en lista med registrerings definitioner.</span><span class="sxs-lookup"><span data-stu-id="1ae86-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1ae86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ae86-104">SYNTAX</span></span>

### <span data-ttu-id="1ae86-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1ae86-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae86-106">Vis</span><span class="sxs-lookup"><span data-stu-id="1ae86-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae86-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ae86-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae86-108">Hämtar en särskild registrerings definition eller en lista med registrerings definitioner.</span><span class="sxs-lookup"><span data-stu-id="1ae86-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1ae86-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ae86-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae86-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ae86-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1ae86-111">Hämtar alla registrerings definitioner i standard omfattning.</span><span class="sxs-lookup"><span data-stu-id="1ae86-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="1ae86-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1ae86-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1ae86-113">Hämtar registrerings definitionen efter namn i standard omfattning.</span><span class="sxs-lookup"><span data-stu-id="1ae86-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="1ae86-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1ae86-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1ae86-115">Hämtar alla registrerings definitioner vid det givna omfånget.</span><span class="sxs-lookup"><span data-stu-id="1ae86-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="1ae86-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ae86-116">PARAMETERS</span></span>

### <span data-ttu-id="1ae86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae86-117">-DefaultProfile</span></span>
<span data-ttu-id="1ae86-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae86-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ae86-119">-Name</span></span>
<span data-ttu-id="1ae86-120">Det unika namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="1ae86-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae86-121">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1ae86-121">-Scope</span></span>
<span data-ttu-id="1ae86-122">Omfattningen där registrerings definitionen skapades.</span><span class="sxs-lookup"><span data-stu-id="1ae86-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae86-123">CommonParameters</span></span>
<span data-ttu-id="1ae86-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae86-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ae86-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae86-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ae86-126">INPUTS</span></span>

### <span data-ttu-id="1ae86-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="1ae86-127">None</span></span>
## <span data-ttu-id="1ae86-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ae86-128">OUTPUTS</span></span>

### <span data-ttu-id="1ae86-129">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae86-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="1ae86-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ae86-130">NOTES</span></span>

## <span data-ttu-id="1ae86-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ae86-131">RELATED LINKS</span></span>