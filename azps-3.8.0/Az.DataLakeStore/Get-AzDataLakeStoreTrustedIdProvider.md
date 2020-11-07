---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926710"
---
# <span data-ttu-id="ec64b-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ec64b-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ec64b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec64b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec64b-103">Hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec64b-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ec64b-104">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="ec64b-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="ec64b-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec64b-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec64b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec64b-106">DESCRIPTION</span></span>
<span data-ttu-id="ec64b-107">Cmdleten **Get-AzDataLakeStoreTrustedIdProvider** hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ec64b-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ec64b-108">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="ec64b-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="ec64b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec64b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec64b-110">Exempel 1: skaffa en särskild betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="ec64b-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="ec64b-111">Returnerar leverantören med namnet "$" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ec64b-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="ec64b-112">Exempel 2: lista alla leverantörer i ett konto</span><span class="sxs-lookup"><span data-stu-id="ec64b-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="ec64b-113">Visar alla leverantörer under kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ec64b-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="ec64b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec64b-114">PARAMETERS</span></span>

### <span data-ttu-id="ec64b-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="ec64b-115">-Account</span></span>
<span data-ttu-id="ec64b-116">Data Lake Store-konto för att hämta den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="ec64b-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="ec64b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec64b-117">-DefaultProfile</span></span>
<span data-ttu-id="ec64b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ec64b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec64b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec64b-119">-Name</span></span>
<span data-ttu-id="ec64b-120">Namnet på den betrodda identitets leverantör som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="ec64b-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="ec64b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec64b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec64b-122">Namn på resurs gruppen som du vill hämta angivet konto för betrodd identitets leverantör för.</span><span class="sxs-lookup"><span data-stu-id="ec64b-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="ec64b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec64b-123">CommonParameters</span></span>
<span data-ttu-id="ec64b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec64b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec64b-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec64b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec64b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec64b-126">INPUTS</span></span>

### <span data-ttu-id="ec64b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ec64b-127">System.String</span></span>

## <span data-ttu-id="ec64b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec64b-128">OUTPUTS</span></span>

### <span data-ttu-id="ec64b-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ec64b-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ec64b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec64b-130">NOTES</span></span>

## <span data-ttu-id="ec64b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec64b-131">RELATED LINKS</span></span>
