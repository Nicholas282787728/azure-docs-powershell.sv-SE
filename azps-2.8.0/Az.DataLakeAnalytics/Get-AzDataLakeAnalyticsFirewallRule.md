---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 37c14547712233a025da56180e7a362f25168400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744650"
---
# <span data-ttu-id="d8b38-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8b38-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d8b38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8b38-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b38-103">Hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="d8b38-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d8b38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8b38-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8b38-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b38-106">Cmdleten **Get-AzDataLakeAnalyticsFirewallRule** hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="d8b38-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d8b38-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8b38-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b38-108">Exempel 1: skaffa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="d8b38-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="d8b38-109">Det här kommandot får brand Väggs regeln "brand Väggs regel" från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="d8b38-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="d8b38-110">Exempel 2: Visa alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="d8b38-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="d8b38-111">Det här kommandot får alla brand Väggs regler från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="d8b38-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="d8b38-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8b38-112">PARAMETERS</span></span>

### <span data-ttu-id="d8b38-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="d8b38-113">-Account</span></span>
<span data-ttu-id="d8b38-114">Data Lake Analytics-konto för att hämta brand Väggs regeln från</span><span class="sxs-lookup"><span data-stu-id="d8b38-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="d8b38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b38-115">-DefaultProfile</span></span>
<span data-ttu-id="d8b38-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8b38-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b38-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8b38-117">-Name</span></span>
<span data-ttu-id="d8b38-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d8b38-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d8b38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b38-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8b38-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="d8b38-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="d8b38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b38-121">CommonParameters</span></span>
<span data-ttu-id="d8b38-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b38-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b38-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b38-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8b38-124">INPUTS</span></span>

### <span data-ttu-id="d8b38-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b38-125">System.String</span></span>

## <span data-ttu-id="d8b38-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8b38-126">OUTPUTS</span></span>

### <span data-ttu-id="d8b38-127">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d8b38-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d8b38-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8b38-128">NOTES</span></span>

## <span data-ttu-id="d8b38-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8b38-129">RELATED LINKS</span></span>
