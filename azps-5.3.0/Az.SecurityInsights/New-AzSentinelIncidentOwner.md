---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525572"
---
# <span data-ttu-id="ff7a9-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="ff7a9-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="ff7a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7a9-103">Skapa ett incident ägar objekt för att uppdatera en incident ägare.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="ff7a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff7a9-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ff7a9-106">Cmdleten **New-AzSentinelIncidentOwner** skapar ett incident ägar objekt i minnet för att uppdatera ett samtal.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="ff7a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff7a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ff7a9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ff7a9-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="ff7a9-109">I det här exemplet skapas en **IncidentOwner** och en incident uppdateras till den nya ägaren.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="ff7a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff7a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ff7a9-111">-Tilldelat</span><span class="sxs-lookup"><span data-stu-id="ff7a9-111">-AssignedTo</span></span>
<span data-ttu-id="ff7a9-112">Incident ägare-tilldelad</span><span class="sxs-lookup"><span data-stu-id="ff7a9-112">Incident Owner - Assigned To</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7a9-113">-DefaultProfile</span></span>
<span data-ttu-id="ff7a9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff7a9-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="ff7a9-115">-Email</span></span>
<span data-ttu-id="ff7a9-116">Incident ägare – e-post</span><span class="sxs-lookup"><span data-stu-id="ff7a9-116">Incident Owner - Email</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7a9-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ff7a9-117">-ObjectId</span></span>
<span data-ttu-id="ff7a9-118">Incident ägare – ObjectId</span><span class="sxs-lookup"><span data-stu-id="ff7a9-118">Incident Owner - ObjectId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7a9-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ff7a9-119">-UserPrincipalName</span></span>
<span data-ttu-id="ff7a9-120">Incident ägare – användarens huvud namn</span><span class="sxs-lookup"><span data-stu-id="ff7a9-120">Incident Owner - User Principal Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7a9-121">CommonParameters</span></span>
<span data-ttu-id="ff7a9-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7a9-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff7a9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7a9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff7a9-124">INPUTS</span></span>

### <span data-ttu-id="ff7a9-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff7a9-125">None</span></span>
## <span data-ttu-id="ff7a9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff7a9-126">OUTPUTS</span></span>

### <span data-ttu-id="ff7a9-127">Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="ff7a9-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="ff7a9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff7a9-128">NOTES</span></span>

## <span data-ttu-id="ff7a9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff7a9-129">RELATED LINKS</span></span>
