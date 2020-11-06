---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582479"
---
# <span data-ttu-id="926db-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="926db-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="926db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="926db-102">SYNOPSIS</span></span>
<span data-ttu-id="926db-103">Hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="926db-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="926db-104">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="926db-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926db-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="926db-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926db-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="926db-106">DESCRIPTION</span></span>
<span data-ttu-id="926db-107">Cmdleten **Get-AzureRmDataLakeStoreTrustedIdProvider** hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="926db-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="926db-108">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="926db-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="926db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="926db-109">EXAMPLES</span></span>

### <span data-ttu-id="926db-110">Exempel 1: skaffa en särskild betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="926db-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="926db-111">Returnerar leverantören med namnet "$" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="926db-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="926db-112">Exempel 2: lista alla leverantörer i ett konto</span><span class="sxs-lookup"><span data-stu-id="926db-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="926db-113">Visar alla leverantörer under kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="926db-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="926db-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="926db-114">PARAMETERS</span></span>

### <span data-ttu-id="926db-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="926db-115">-Account</span></span>
<span data-ttu-id="926db-116">Data Lake Store-konto för att hämta den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="926db-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="926db-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="926db-117">-Name</span></span>
<span data-ttu-id="926db-118">Namnet på den betrodda identitets leverantör som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="926db-118">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="926db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926db-119">-ResourceGroupName</span></span>
<span data-ttu-id="926db-120">Namn på resurs gruppen som du vill hämta angivet konto för betrodd identitets leverantör för.</span><span class="sxs-lookup"><span data-stu-id="926db-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="926db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926db-121">-DefaultProfile</span></span>
<span data-ttu-id="926db-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="926db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926db-123">CommonParameters</span></span>
<span data-ttu-id="926db-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926db-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926db-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="926db-126">INPUTS</span></span>

## <span data-ttu-id="926db-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="926db-127">OUTPUTS</span></span>

### <span data-ttu-id="926db-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="926db-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="926db-129">Information om den angivna betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="926db-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="926db-130">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="926db-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="926db-131">Listan över betrodda identitets leverantörer i angivet konto.</span><span class="sxs-lookup"><span data-stu-id="926db-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="926db-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="926db-132">NOTES</span></span>

## <span data-ttu-id="926db-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="926db-133">RELATED LINKS</span></span>

