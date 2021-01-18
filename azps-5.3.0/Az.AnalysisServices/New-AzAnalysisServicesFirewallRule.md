---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523292"
---
# <span data-ttu-id="b75f7-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b75f7-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b75f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b75f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b75f7-103">Skapar en ny regel för Analysis Services-brandväggen</span><span class="sxs-lookup"><span data-stu-id="b75f7-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="b75f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b75f7-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b75f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b75f7-106">New-AzAnalysisServicesFirewallRule skapar ett nytt brand Väggs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="b75f7-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="b75f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b75f7-107">EXAMPLES</span></span>

### <span data-ttu-id="b75f7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b75f7-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="b75f7-109">Skapar en brand Väggs regel med namnet rule1 med startintervallet 0.0.0.0 och slut intervall 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="b75f7-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="b75f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b75f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b75f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75f7-111">-DefaultProfile</span></span>
<span data-ttu-id="b75f7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b75f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75f7-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b75f7-113">-FirewallRuleName</span></span>
<span data-ttu-id="b75f7-114">Namn på brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b75f7-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75f7-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="b75f7-115">-RangeEnd</span></span>
<span data-ttu-id="b75f7-116">Intervallet för en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b75f7-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75f7-117">-Rang</span><span class="sxs-lookup"><span data-stu-id="b75f7-117">-RangeStart</span></span>
<span data-ttu-id="b75f7-118">Intervallet början av en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b75f7-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75f7-119">CommonParameters</span></span>
<span data-ttu-id="b75f7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75f7-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75f7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75f7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b75f7-122">INPUTS</span></span>

### <span data-ttu-id="b75f7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b75f7-123">System.String</span></span>

## <span data-ttu-id="b75f7-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b75f7-124">OUTPUTS</span></span>

### <span data-ttu-id="b75f7-125">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b75f7-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b75f7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b75f7-126">NOTES</span></span>

## <span data-ttu-id="b75f7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b75f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="b75f7-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b75f7-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)