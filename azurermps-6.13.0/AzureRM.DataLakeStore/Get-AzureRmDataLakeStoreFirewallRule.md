---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 191b1ebc1f83387a9cf1ac59f6fb3f7a55f115ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573977"
---
# <span data-ttu-id="4db92-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4db92-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4db92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4db92-102">SYNOPSIS</span></span>
<span data-ttu-id="4db92-103">Hämtar de angivna brand Väggs reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4db92-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4db92-104">Om ingen brand Väggs regel anges visas en lista med alla brand Väggs regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="4db92-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4db92-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4db92-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4db92-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4db92-106">DESCRIPTION</span></span>
<span data-ttu-id="4db92-107">Den Get-AzureRmDataLakeStoreFirewallRule cmdleten hämtar de angivna brand Väggs reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4db92-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4db92-108">Om ingen brand Väggs regel anges visas en lista med alla brand Väggs regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="4db92-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="4db92-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4db92-109">EXAMPLES</span></span>

### <span data-ttu-id="4db92-110">Exempel 1: Hämta en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="4db92-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="4db92-111">Returnerar brand Väggs regeln med namnet "MyFirewallRule" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="4db92-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="4db92-112">Exempel 2: Visa alla brand Väggs regler i ett konto</span><span class="sxs-lookup"><span data-stu-id="4db92-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="4db92-113">Returnerar alla brand Väggs regler i kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="4db92-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="4db92-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4db92-114">PARAMETERS</span></span>

### <span data-ttu-id="4db92-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="4db92-115">-Account</span></span>
<span data-ttu-id="4db92-116">Det data Lake Store-konto som brand Väggs regeln hämtas från.</span><span class="sxs-lookup"><span data-stu-id="4db92-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="4db92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db92-117">-DefaultProfile</span></span>
<span data-ttu-id="4db92-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4db92-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db92-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4db92-119">-Name</span></span>
<span data-ttu-id="4db92-120">Namnet på brand Väggs regeln som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="4db92-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="4db92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db92-121">-ResourceGroupName</span></span>
<span data-ttu-id="4db92-122">Namnet på den resurs grupp som du vill hämta angivet kontos brand Väggs regel under.</span><span class="sxs-lookup"><span data-stu-id="4db92-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="4db92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db92-123">CommonParameters</span></span>
<span data-ttu-id="4db92-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db92-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db92-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db92-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4db92-126">INPUTS</span></span>

### <span data-ttu-id="4db92-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4db92-127">System.String</span></span>

## <span data-ttu-id="4db92-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4db92-128">OUTPUTS</span></span>

### <span data-ttu-id="4db92-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4db92-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4db92-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4db92-130">NOTES</span></span>

## <span data-ttu-id="4db92-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4db92-131">RELATED LINKS</span></span>
