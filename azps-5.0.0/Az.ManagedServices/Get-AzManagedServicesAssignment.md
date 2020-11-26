---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270570"
---
# <span data-ttu-id="fc348-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="fc348-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="fc348-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc348-102">SYNOPSIS</span></span>
<span data-ttu-id="fc348-103">Hämtar en specifik registrerings uppgift eller en lista med registrerings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="fc348-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="fc348-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc348-104">SYNTAX</span></span>

### <span data-ttu-id="fc348-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="fc348-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc348-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fc348-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc348-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc348-107">DESCRIPTION</span></span>
<span data-ttu-id="fc348-108">Hämtar en specifik registrerings uppgift eller en lista med registrerings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="fc348-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="fc348-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc348-109">EXAMPLES</span></span>

### <span data-ttu-id="fc348-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc348-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fc348-111">Hämtar alla registrerings uppgifter under standard omfattningen.</span><span class="sxs-lookup"><span data-stu-id="fc348-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="fc348-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fc348-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="fc348-113">Hämtar alla registrerings uppgifter med information om registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="fc348-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="fc348-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fc348-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fc348-115">Hämtar en registrerings tilldelning med namn utan registrerings information.</span><span class="sxs-lookup"><span data-stu-id="fc348-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="fc348-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="fc348-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="fc348-117">Hämtar en registrerings tilldelning med namn med registrerings definitions uppgifter.</span><span class="sxs-lookup"><span data-stu-id="fc348-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="fc348-118">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="fc348-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fc348-119">Hämtar alla registrerings tilldelningar i angivet omfattning.</span><span class="sxs-lookup"><span data-stu-id="fc348-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="fc348-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc348-120">PARAMETERS</span></span>

### <span data-ttu-id="fc348-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc348-121">-DefaultProfile</span></span>
<span data-ttu-id="fc348-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc348-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc348-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="fc348-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="fc348-124">Om registrerings information ska tas med.</span><span class="sxs-lookup"><span data-stu-id="fc348-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc348-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc348-125">-Name</span></span>
<span data-ttu-id="fc348-126">Det unika namnet på registrerings uppgiften.</span><span class="sxs-lookup"><span data-stu-id="fc348-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="fc348-127">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="fc348-127">-Scope</span></span>
<span data-ttu-id="fc348-128">Omfattningen där registrerings uppgiften skapades.</span><span class="sxs-lookup"><span data-stu-id="fc348-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="fc348-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc348-129">CommonParameters</span></span>
<span data-ttu-id="fc348-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc348-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc348-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc348-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc348-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc348-132">INPUTS</span></span>

### <span data-ttu-id="fc348-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="fc348-133">None</span></span>
## <span data-ttu-id="fc348-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc348-134">OUTPUTS</span></span>

### <span data-ttu-id="fc348-135">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="fc348-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="fc348-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc348-136">NOTES</span></span>

## <span data-ttu-id="fc348-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc348-137">RELATED LINKS</span></span>