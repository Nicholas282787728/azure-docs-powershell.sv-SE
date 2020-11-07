---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 302ad6ac14ad9fcb08053e70afb7951e72c6e027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577235"
---
# <span data-ttu-id="6f188-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6f188-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6f188-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f188-102">SYNOPSIS</span></span>
<span data-ttu-id="6f188-103">Lägger till en betrodd identitets leverantör till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="6f188-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f188-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f188-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f188-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f188-105">DESCRIPTION</span></span>
<span data-ttu-id="6f188-106">Cmdleten **Add-AzureRmDataLakeStoreTrustedIdProvider** lägger till en betrodd identitets tjänst till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="6f188-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6f188-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f188-107">EXAMPLES</span></span>

### <span data-ttu-id="6f188-108">Exempel 1: lägga till en betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="6f188-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="6f188-109">Lägger till leverantören "" ContosoADL "med leverantörens slut punkt" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="6f188-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="6f188-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f188-110">PARAMETERS</span></span>

### <span data-ttu-id="6f188-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="6f188-111">-Account</span></span>
<span data-ttu-id="6f188-112">Namnet på data Lake Store-kontot där den angivna betrodda identitets leverantören ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6f188-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="6f188-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f188-113">-DefaultProfile</span></span>
<span data-ttu-id="6f188-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f188-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f188-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f188-115">-Name</span></span>
<span data-ttu-id="6f188-116">Namnet på den betrodda identitets leverantör som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="6f188-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f188-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f188-117">-ProviderEndpoint</span></span>
<span data-ttu-id="6f188-118">Den giltiga förlitande leverantörens slut punkt i formatet: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="6f188-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f188-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f188-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f188-120">Namnet på den resurs grupp under vilken kontot för att lägga till den betrodda identitets leverantören är.</span><span class="sxs-lookup"><span data-stu-id="6f188-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f188-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f188-121">-Confirm</span></span>
<span data-ttu-id="6f188-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f188-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f188-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f188-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f188-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f188-124">CommonParameters</span></span>
<span data-ttu-id="6f188-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f188-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f188-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f188-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f188-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f188-127">INPUTS</span></span>

### <span data-ttu-id="6f188-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="6f188-128">None</span></span>
<span data-ttu-id="6f188-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6f188-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f188-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f188-130">OUTPUTS</span></span>

### <span data-ttu-id="6f188-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6f188-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="6f188-132">Den bevarade pålitlige identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="6f188-132">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="6f188-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f188-133">NOTES</span></span>

## <span data-ttu-id="6f188-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f188-134">RELATED LINKS</span></span>
