---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520204"
---
# <span data-ttu-id="e50a1-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e50a1-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e50a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e50a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e50a1-103">Lägger till en betrodd identitets leverantör till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e50a1-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="e50a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e50a1-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e50a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e50a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e50a1-106">Cmdleten **Add-AzDataLakeStoreTrustedIdProvider** lägger till en betrodd identitets tjänst till det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e50a1-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="e50a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e50a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e50a1-108">Exempel 1: lägga till en betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="e50a1-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="e50a1-109">Lägger till leverantören "" ContosoADL "med leverantörens slut punkt" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="e50a1-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="e50a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e50a1-110">PARAMETERS</span></span>

### <span data-ttu-id="e50a1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e50a1-111">-Account</span></span>
<span data-ttu-id="e50a1-112">Namnet på data Lake Store-kontot där den angivna betrodda identitets leverantören ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e50a1-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="e50a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50a1-113">-DefaultProfile</span></span>
<span data-ttu-id="e50a1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e50a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e50a1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e50a1-115">-Name</span></span>
<span data-ttu-id="e50a1-116">Namnet på den betrodda identitets leverantör som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="e50a1-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="e50a1-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="e50a1-117">-ProviderEndpoint</span></span>
<span data-ttu-id="e50a1-118">Den giltiga förlitande leverantörens slut punkt i formatet: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="e50a1-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="e50a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="e50a1-120">Namnet på den resurs grupp under vilken kontot för att lägga till den betrodda identitets leverantören är.</span><span class="sxs-lookup"><span data-stu-id="e50a1-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="e50a1-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e50a1-121">-Confirm</span></span>
<span data-ttu-id="e50a1-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e50a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50a1-123">-WhatIf</span></span>
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

### <span data-ttu-id="e50a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50a1-124">CommonParameters</span></span>
<span data-ttu-id="e50a1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50a1-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50a1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50a1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e50a1-127">INPUTS</span></span>

### <span data-ttu-id="e50a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e50a1-128">System.String</span></span>

## <span data-ttu-id="e50a1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e50a1-129">OUTPUTS</span></span>

### <span data-ttu-id="e50a1-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e50a1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e50a1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e50a1-131">NOTES</span></span>

## <span data-ttu-id="e50a1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e50a1-132">RELATED LINKS</span></span>
