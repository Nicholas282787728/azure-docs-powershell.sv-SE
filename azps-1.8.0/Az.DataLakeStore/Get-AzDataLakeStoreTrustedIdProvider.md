---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916878"
---
# <span data-ttu-id="ff043-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ff043-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ff043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff043-102">SYNOPSIS</span></span>
<span data-ttu-id="ff043-103">Hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff043-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ff043-104">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="ff043-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="ff043-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff043-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff043-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff043-106">DESCRIPTION</span></span>
<span data-ttu-id="ff043-107">Cmdleten **Get-AzDataLakeStoreTrustedIdProvider** hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff043-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="ff043-108">Om ingen leverantör anges visas alla providrar för kontot.</span><span class="sxs-lookup"><span data-stu-id="ff043-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="ff043-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff043-109">EXAMPLES</span></span>

### <span data-ttu-id="ff043-110">Exempel 1: skaffa en särskild betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="ff043-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="ff043-111">Returnerar leverantören med namnet "$" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ff043-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="ff043-112">Exempel 2: lista alla leverantörer i ett konto</span><span class="sxs-lookup"><span data-stu-id="ff043-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="ff043-113">Visar alla leverantörer under kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ff043-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="ff043-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff043-114">PARAMETERS</span></span>

### <span data-ttu-id="ff043-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="ff043-115">-Account</span></span>
<span data-ttu-id="ff043-116">Data Lake Store-konto för att hämta den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="ff043-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="ff043-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff043-117">-DefaultProfile</span></span>
<span data-ttu-id="ff043-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff043-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff043-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff043-119">-Name</span></span>
<span data-ttu-id="ff043-120">Namnet på den betrodda identitets leverantör som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="ff043-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="ff043-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff043-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff043-122">Namn på resurs gruppen som du vill hämta angivet konto för betrodd identitets leverantör för.</span><span class="sxs-lookup"><span data-stu-id="ff043-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="ff043-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff043-123">CommonParameters</span></span>
<span data-ttu-id="ff043-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff043-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff043-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff043-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff043-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff043-126">INPUTS</span></span>

### <span data-ttu-id="ff043-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ff043-127">System.String</span></span>

## <span data-ttu-id="ff043-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff043-128">OUTPUTS</span></span>

### <span data-ttu-id="ff043-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ff043-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ff043-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff043-130">NOTES</span></span>

## <span data-ttu-id="ff043-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff043-131">RELATED LINKS</span></span>