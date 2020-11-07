---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756132"
---
# <span data-ttu-id="b9416-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b9416-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b9416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9416-102">SYNOPSIS</span></span>
<span data-ttu-id="b9416-103">Hämtar de konfigurerade inställningarna för säkerhets arbets ytan för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b9416-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9416-104">SYNTAX</span></span>

### <span data-ttu-id="b9416-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="b9416-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9416-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b9416-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9416-107">ID</span><span class="sxs-lookup"><span data-stu-id="b9416-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9416-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9416-108">DESCRIPTION</span></span>
<span data-ttu-id="b9416-109">Denna cmdlet gör att du kan upptäcka den konfigurerade arbets ytan som innehåller säkerhets data som samlats in av säkerhets agenten som är installerad på virtuella datorer i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b9416-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="b9416-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9416-110">EXAMPLES</span></span>

### <span data-ttu-id="b9416-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b9416-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="b9416-112">Hämtar arbets ytans inställningar för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b9416-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="b9416-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9416-113">PARAMETERS</span></span>

### <span data-ttu-id="b9416-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9416-114">-DefaultProfile</span></span>
<span data-ttu-id="b9416-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9416-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9416-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9416-116">-Name</span></span>
<span data-ttu-id="b9416-117">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b9416-117">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9416-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9416-118">-ResourceId</span></span>
<span data-ttu-id="b9416-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b9416-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9416-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9416-120">CommonParameters</span></span>
<span data-ttu-id="b9416-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9416-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9416-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9416-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9416-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9416-123">INPUTS</span></span>

### <span data-ttu-id="b9416-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b9416-124">System.String</span></span>

## <span data-ttu-id="b9416-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9416-125">OUTPUTS</span></span>

### <span data-ttu-id="b9416-126">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b9416-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b9416-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9416-127">NOTES</span></span>

## <span data-ttu-id="b9416-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9416-128">RELATED LINKS</span></span>
