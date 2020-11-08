---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: dc315e2ee69fbccd12ed1f07057e51dab30c04e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916917"
---
# <span data-ttu-id="daaa9-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="daaa9-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="daaa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="daaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="daaa9-103">Lägger till en betrodd identitets leverantör till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="daaa9-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="daaa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="daaa9-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daaa9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="daaa9-105">DESCRIPTION</span></span>
<span data-ttu-id="daaa9-106">Cmdleten **Add-AzDataLakeStoreTrustedIdProvider** lägger till en betrodd identitets tjänst till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="daaa9-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="daaa9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="daaa9-107">EXAMPLES</span></span>

### <span data-ttu-id="daaa9-108">Exempel 1: lägga till en betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="daaa9-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="daaa9-109">Lägger till leverantören "" ContosoADL "med leverantörens slut punkt" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="daaa9-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="daaa9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="daaa9-110">PARAMETERS</span></span>

### <span data-ttu-id="daaa9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="daaa9-111">-Account</span></span>
<span data-ttu-id="daaa9-112">Namnet på data Lake Store-kontot där den angivna betrodda identitets leverantören ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="daaa9-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="daaa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daaa9-113">-DefaultProfile</span></span>
<span data-ttu-id="daaa9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="daaa9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daaa9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="daaa9-115">-Name</span></span>
<span data-ttu-id="daaa9-116">Namnet på den betrodda identitets leverantör som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="daaa9-116">The name of the trusted identity provider to add</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daaa9-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="daaa9-117">-ProviderEndpoint</span></span>
<span data-ttu-id="daaa9-118">Den giltiga förlitade leverantörens slut punkt i formatet: https://sts.windows.net/\<provider identitet \></span><span class="sxs-lookup"><span data-stu-id="daaa9-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daaa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daaa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="daaa9-120">Namnet på den resurs grupp under vilken kontot för att lägga till den betrodda identitets leverantören är.</span><span class="sxs-lookup"><span data-stu-id="daaa9-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daaa9-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="daaa9-121">-Confirm</span></span>
<span data-ttu-id="daaa9-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="daaa9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaa9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daaa9-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daaa9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaa9-124">CommonParameters</span></span>
<span data-ttu-id="daaa9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daaa9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaa9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daaa9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaa9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="daaa9-127">INPUTS</span></span>

### <span data-ttu-id="daaa9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="daaa9-128">System.String</span></span>

## <span data-ttu-id="daaa9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="daaa9-129">OUTPUTS</span></span>

### <span data-ttu-id="daaa9-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="daaa9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="daaa9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="daaa9-131">NOTES</span></span>

## <span data-ttu-id="daaa9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="daaa9-132">RELATED LINKS</span></span>