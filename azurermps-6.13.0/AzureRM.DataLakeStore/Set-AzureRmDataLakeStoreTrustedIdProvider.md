---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 509c80f77d48cebd101703727cefb37399ed2577
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576307"
---
# <span data-ttu-id="2490a-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2490a-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2490a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2490a-102">SYNOPSIS</span></span>
<span data-ttu-id="2490a-103">Ändrar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2490a-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2490a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2490a-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2490a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2490a-105">DESCRIPTION</span></span>
<span data-ttu-id="2490a-106">Cmdleten **set-AzureRmDataLakeStoreTrustedIdProvider** ändrar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2490a-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2490a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2490a-107">EXAMPLES</span></span>

### <span data-ttu-id="2490a-108">Exempel 1: uppdatera slut punkten för en betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="2490a-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="2490a-109">Då uppdateras leverantörens endpoing för brand Väggs regel "" ContosoADL "till" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="2490a-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="2490a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2490a-110">PARAMETERS</span></span>

### <span data-ttu-id="2490a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2490a-111">-Account</span></span>
<span data-ttu-id="2490a-112">Data Lake Store-konto för att lägga till den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="2490a-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="2490a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2490a-113">-DefaultProfile</span></span>
<span data-ttu-id="2490a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2490a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2490a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2490a-115">-Name</span></span>
<span data-ttu-id="2490a-116">Namnet på den betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="2490a-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="2490a-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="2490a-117">-ProviderEndpoint</span></span>
<span data-ttu-id="2490a-118">Den giltiga betrodda leverantörens slut punkter i formatet: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="2490a-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="2490a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2490a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2490a-120">Anger namnet på den resurs grupp som innehåller kontot som ska uppdatera den betrodda identitets leverantören för.</span><span class="sxs-lookup"><span data-stu-id="2490a-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="2490a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2490a-121">-Confirm</span></span>
<span data-ttu-id="2490a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2490a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2490a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2490a-123">-WhatIf</span></span>
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

### <span data-ttu-id="2490a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2490a-124">CommonParameters</span></span>
<span data-ttu-id="2490a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2490a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2490a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2490a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2490a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2490a-127">INPUTS</span></span>

### <span data-ttu-id="2490a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2490a-128">System.String</span></span>

## <span data-ttu-id="2490a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2490a-129">OUTPUTS</span></span>

### <span data-ttu-id="2490a-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2490a-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2490a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2490a-131">NOTES</span></span>

## <span data-ttu-id="2490a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2490a-132">RELATED LINKS</span></span>
