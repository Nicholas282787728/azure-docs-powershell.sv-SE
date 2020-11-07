---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 485f244caa78bffda71d6129990c76daa8b173c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922541"
---
# <span data-ttu-id="764f5-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="764f5-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="764f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="764f5-102">SYNOPSIS</span></span>
<span data-ttu-id="764f5-103">Skapar ett objekt av typen Azns-åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="764f5-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="764f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="764f5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="764f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="764f5-105">DESCRIPTION</span></span>
<span data-ttu-id="764f5-106">Skapar ett objekt av typen Azns-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="764f5-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="764f5-107">Det här objektet måste skickas till det kommando som skapar en regel för loggnings varning.</span><span class="sxs-lookup"><span data-stu-id="764f5-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="764f5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="764f5-108">EXAMPLES</span></span>

### <span data-ttu-id="764f5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="764f5-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="764f5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="764f5-110">PARAMETERS</span></span>

### <span data-ttu-id="764f5-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="764f5-111">-ActionGroup</span></span>
<span data-ttu-id="764f5-112">Listan med åtgärds grupper att skicka meddelande till</span><span class="sxs-lookup"><span data-stu-id="764f5-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764f5-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="764f5-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="764f5-114">Den anpassade webhook-nyttolasten</span><span class="sxs-lookup"><span data-stu-id="764f5-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="764f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764f5-115">-DefaultProfile</span></span>
<span data-ttu-id="764f5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="764f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="764f5-117">-Postämne</span><span class="sxs-lookup"><span data-stu-id="764f5-117">-EmailSubject</span></span>
<span data-ttu-id="764f5-118">E-postmeddelandets ämne</span><span class="sxs-lookup"><span data-stu-id="764f5-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="764f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764f5-119">CommonParameters</span></span>
<span data-ttu-id="764f5-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764f5-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="764f5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764f5-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="764f5-122">INPUTS</span></span>

### <span data-ttu-id="764f5-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="764f5-123">None</span></span>

## <span data-ttu-id="764f5-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="764f5-124">OUTPUTS</span></span>

### <span data-ttu-id="764f5-125">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="764f5-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="764f5-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="764f5-126">NOTES</span></span>

## <span data-ttu-id="764f5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="764f5-127">RELATED LINKS</span></span>
