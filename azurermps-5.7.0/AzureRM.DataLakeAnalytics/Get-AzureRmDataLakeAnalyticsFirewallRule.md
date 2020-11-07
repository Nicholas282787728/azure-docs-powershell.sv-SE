---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 49ddf65a5c32bafab32945b6d5114f65e3c59047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755248"
---
# <span data-ttu-id="26338-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="26338-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="26338-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26338-102">SYNOPSIS</span></span>
<span data-ttu-id="26338-103">Hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="26338-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26338-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26338-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26338-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26338-105">DESCRIPTION</span></span>
<span data-ttu-id="26338-106">Cmdleten **Get-AzureRmDataLakeAnalyticsFirewallRule** hämtar en brand Väggs regel eller en lista med brand Väggs regler från ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="26338-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="26338-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26338-107">EXAMPLES</span></span>

### <span data-ttu-id="26338-108">Exempel 1: skaffa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="26338-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="26338-109">Det här kommandot får brand Väggs regeln "brand Väggs regel" från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="26338-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="26338-110">Exempel 2: Visa alla brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="26338-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="26338-111">Det här kommandot får alla brand Väggs regler från kontot "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="26338-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="26338-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26338-112">PARAMETERS</span></span>

### <span data-ttu-id="26338-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="26338-113">-Account</span></span>
<span data-ttu-id="26338-114">Data Lake Analytics-konto för att hämta brand Väggs regeln från</span><span class="sxs-lookup"><span data-stu-id="26338-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26338-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26338-115">-DefaultProfile</span></span>
<span data-ttu-id="26338-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26338-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26338-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="26338-117">-Name</span></span>
<span data-ttu-id="26338-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="26338-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26338-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26338-119">-ResourceGroupName</span></span>
<span data-ttu-id="26338-120">Namnet på den resurs grupp som du vill hämta kontot för.</span><span class="sxs-lookup"><span data-stu-id="26338-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26338-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26338-121">CommonParameters</span></span>
<span data-ttu-id="26338-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26338-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26338-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26338-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26338-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26338-124">INPUTS</span></span>

### <span data-ttu-id="26338-125">System. String</span><span class="sxs-lookup"><span data-stu-id="26338-125">System.String</span></span>

## <span data-ttu-id="26338-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26338-126">OUTPUTS</span></span>

### <span data-ttu-id="26338-127">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="26338-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="26338-128">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule, Microsoft. Azure. commands. DataLakeAnalytics, version = 2.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26338-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="26338-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26338-129">NOTES</span></span>

## <span data-ttu-id="26338-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26338-130">RELATED LINKS</span></span>
