---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 274a751130d5dba8d246a2f02f72be815f889378
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746965"
---
# <span data-ttu-id="e98ee-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e98ee-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e98ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e98ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e98ee-103">Hämtar de konfigurerade inställningarna för säkerhets arbets ytan för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e98ee-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="e98ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e98ee-104">SYNTAX</span></span>

### <span data-ttu-id="e98ee-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="e98ee-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98ee-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e98ee-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98ee-107">ID</span><span class="sxs-lookup"><span data-stu-id="e98ee-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e98ee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e98ee-108">DESCRIPTION</span></span>
<span data-ttu-id="e98ee-109">Denna cmdlet gör att du kan upptäcka den konfigurerade arbets ytan som innehåller säkerhets data som samlats in av säkerhets agenten som är installerad på virtuella datorer i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e98ee-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="e98ee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e98ee-110">EXAMPLES</span></span>

### <span data-ttu-id="e98ee-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e98ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="e98ee-112">Hämtar arbets ytans inställningar för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e98ee-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="e98ee-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e98ee-113">PARAMETERS</span></span>

### <span data-ttu-id="e98ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98ee-114">-DefaultProfile</span></span>
<span data-ttu-id="e98ee-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e98ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98ee-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e98ee-116">-Name</span></span>
<span data-ttu-id="e98ee-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e98ee-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98ee-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98ee-118">-ResourceId</span></span>
<span data-ttu-id="e98ee-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e98ee-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98ee-120">CommonParameters</span></span>
<span data-ttu-id="e98ee-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98ee-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e98ee-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98ee-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e98ee-123">INPUTS</span></span>

### <span data-ttu-id="e98ee-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e98ee-124">System.String</span></span>

## <span data-ttu-id="e98ee-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e98ee-125">OUTPUTS</span></span>

### <span data-ttu-id="e98ee-126">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e98ee-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e98ee-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e98ee-127">NOTES</span></span>

## <span data-ttu-id="e98ee-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e98ee-128">RELATED LINKS</span></span>
