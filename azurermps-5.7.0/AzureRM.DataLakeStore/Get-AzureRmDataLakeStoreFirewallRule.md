---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575679"
---
# <span data-ttu-id="4ddc8-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4ddc8-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4ddc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ddc8-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddc8-103">Hämtar de angivna brand Väggs reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4ddc8-104">Om ingen brand Väggs regel anges visas en lista med alla brand Väggs regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ddc8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ddc8-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ddc8-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ddc8-106">DESCRIPTION</span></span>
<span data-ttu-id="4ddc8-107">Den Get-AzureRmDataLakeStoreFirewallRule cmdleten hämtar de angivna brand Väggs reglerna i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4ddc8-108">Om ingen brand Väggs regel anges visas en lista med alla brand Väggs regler för kontot.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="4ddc8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ddc8-109">EXAMPLES</span></span>

### <span data-ttu-id="4ddc8-110">Exempel 1: Hämta en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="4ddc8-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="4ddc8-111">Returnerar brand Väggs regeln med namnet "MyFirewallRule" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="4ddc8-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="4ddc8-112">Exempel 2: Visa alla brand Väggs regler i ett konto</span><span class="sxs-lookup"><span data-stu-id="4ddc8-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="4ddc8-113">Returnerar alla brand Väggs regler i kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="4ddc8-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="4ddc8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ddc8-114">PARAMETERS</span></span>

### <span data-ttu-id="4ddc8-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="4ddc8-115">-Account</span></span>
<span data-ttu-id="4ddc8-116">Det data Lake Store-konto som brand Väggs regeln hämtas från.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="4ddc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ddc8-117">-DefaultProfile</span></span>
<span data-ttu-id="4ddc8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ddc8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ddc8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ddc8-119">-Name</span></span>
<span data-ttu-id="4ddc8-120">Namnet på brand Väggs regeln som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="4ddc8-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="4ddc8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ddc8-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ddc8-122">Namnet på den resurs grupp som du vill hämta angivet kontos brand Väggs regel under.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="4ddc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddc8-123">CommonParameters</span></span>
<span data-ttu-id="4ddc8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddc8-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddc8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddc8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ddc8-126">INPUTS</span></span>

### <span data-ttu-id="4ddc8-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ddc8-127">None</span></span>
<span data-ttu-id="4ddc8-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ddc8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ddc8-129">OUTPUTS</span></span>

### <span data-ttu-id="4ddc8-130">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4ddc8-130">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="4ddc8-131">Den angivna brand Väggs regeln som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="4ddc8-131">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="4ddc8-132">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="4ddc8-132">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="4ddc8-133">Listan med brand Väggs regler i angivet konto.</span><span class="sxs-lookup"><span data-stu-id="4ddc8-133">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="4ddc8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ddc8-134">NOTES</span></span>

## <span data-ttu-id="4ddc8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ddc8-135">RELATED LINKS</span></span>

