---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584356"
---
# <span data-ttu-id="539e5-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="539e5-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="539e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="539e5-102">SYNOPSIS</span></span>
<span data-ttu-id="539e5-103">Hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="539e5-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="539e5-104">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="539e5-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539e5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="539e5-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539e5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="539e5-106">DESCRIPTION</span></span>
<span data-ttu-id="539e5-107">Cmdleten **Get-AzureRmDataLakeStoreTrustedIdProvider** hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="539e5-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="539e5-108">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="539e5-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="539e5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="539e5-109">EXAMPLES</span></span>

### <span data-ttu-id="539e5-110">Exempel 1: skaffa en särskild betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="539e5-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="539e5-111">Returnerar leverantören med namnet "$" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="539e5-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="539e5-112">Exempel 2: lista alla leverantörer i ett konto</span><span class="sxs-lookup"><span data-stu-id="539e5-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="539e5-113">Visar alla leverantörer under kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="539e5-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="539e5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="539e5-114">PARAMETERS</span></span>

### <span data-ttu-id="539e5-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="539e5-115">-Account</span></span>
<span data-ttu-id="539e5-116">Data Lake Store-konto för att hämta den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="539e5-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="539e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539e5-117">-DefaultProfile</span></span>
<span data-ttu-id="539e5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="539e5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="539e5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="539e5-119">-Name</span></span>
<span data-ttu-id="539e5-120">Namnet på den betrodda identitets leverantör som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="539e5-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="539e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="539e5-122">Namn på resurs gruppen som du vill hämta angivet konto för betrodd identitets leverantör för.</span><span class="sxs-lookup"><span data-stu-id="539e5-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="539e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539e5-123">CommonParameters</span></span>
<span data-ttu-id="539e5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539e5-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539e5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="539e5-126">INPUTS</span></span>

### <span data-ttu-id="539e5-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="539e5-127">None</span></span>
<span data-ttu-id="539e5-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="539e5-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="539e5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="539e5-129">OUTPUTS</span></span>

### <span data-ttu-id="539e5-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="539e5-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="539e5-131">Information om den angivna betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="539e5-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="539e5-132">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="539e5-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="539e5-133">Listan över betrodda identitets leverantörer i angivet konto.</span><span class="sxs-lookup"><span data-stu-id="539e5-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="539e5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="539e5-134">NOTES</span></span>

## <span data-ttu-id="539e5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="539e5-135">RELATED LINKS</span></span>

