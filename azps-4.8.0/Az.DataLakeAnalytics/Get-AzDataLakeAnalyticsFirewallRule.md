---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260787"
---
# <span data-ttu-id="65d06-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="65d06-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="65d06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65d06-102">SYNOPSIS</span></span>
<span data-ttu-id="65d06-103">Hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="65d06-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="65d06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65d06-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65d06-105">DESCRIPTION</span></span>
<span data-ttu-id="65d06-106">Cmdleten **Get-AzDataLakeAnalyticsFirewallRule** hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="65d06-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="65d06-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65d06-107">EXAMPLES</span></span>

### <span data-ttu-id="65d06-108">Exempel 1: skaffa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="65d06-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="65d06-109">Det här kommandot får brand Väggs regeln "brand Väggs regel" från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="65d06-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="65d06-110">Exempel 2: Visa alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="65d06-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="65d06-111">Det här kommandot får alla brand Väggs regler från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="65d06-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="65d06-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65d06-112">PARAMETERS</span></span>

### <span data-ttu-id="65d06-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="65d06-113">-Account</span></span>
<span data-ttu-id="65d06-114">Data Lake Analytics-konto för att hämta brand Väggs regeln från</span><span class="sxs-lookup"><span data-stu-id="65d06-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d06-115">-DefaultProfile</span></span>
<span data-ttu-id="65d06-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="65d06-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65d06-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="65d06-117">-Name</span></span>
<span data-ttu-id="65d06-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="65d06-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d06-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d06-119">-ResourceGroupName</span></span>
<span data-ttu-id="65d06-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="65d06-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d06-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d06-121">CommonParameters</span></span>
<span data-ttu-id="65d06-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d06-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d06-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d06-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d06-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65d06-124">INPUTS</span></span>

### <span data-ttu-id="65d06-125">System. String</span><span class="sxs-lookup"><span data-stu-id="65d06-125">System.String</span></span>

## <span data-ttu-id="65d06-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65d06-126">OUTPUTS</span></span>

### <span data-ttu-id="65d06-127">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="65d06-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="65d06-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65d06-128">NOTES</span></span>

## <span data-ttu-id="65d06-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65d06-129">RELATED LINKS</span></span>
