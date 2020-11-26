---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260032"
---
# <span data-ttu-id="3574d-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3574d-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3574d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3574d-102">SYNOPSIS</span></span>
<span data-ttu-id="3574d-103">Ändrar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3574d-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3574d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3574d-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3574d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3574d-105">DESCRIPTION</span></span>
<span data-ttu-id="3574d-106">Cmdleten **set-AzDataLakeStoreTrustedIdProvider** ändrar den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3574d-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3574d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3574d-107">EXAMPLES</span></span>

### <span data-ttu-id="3574d-108">Exempel 1: uppdatera slut punkten för en betrodd identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="3574d-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="3574d-109">Då uppdateras leverantörens slut punkt för brand Väggs regel "" ContosoADL "på" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="3574d-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="3574d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3574d-110">PARAMETERS</span></span>

### <span data-ttu-id="3574d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3574d-111">-Account</span></span>
<span data-ttu-id="3574d-112">Data Lake Store-konto för att lägga till den betrodda identitets leverantören</span><span class="sxs-lookup"><span data-stu-id="3574d-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="3574d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3574d-113">-DefaultProfile</span></span>
<span data-ttu-id="3574d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3574d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3574d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3574d-115">-Name</span></span>
<span data-ttu-id="3574d-116">Namnet på den betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="3574d-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="3574d-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="3574d-117">-ProviderEndpoint</span></span>
<span data-ttu-id="3574d-118">Den giltiga betrodda leverantörens slut punkter i formatet: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="3574d-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="3574d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3574d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3574d-120">Anger namnet på den resurs grupp som innehåller kontot som ska uppdatera den betrodda identitets leverantören för.</span><span class="sxs-lookup"><span data-stu-id="3574d-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="3574d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3574d-121">-Confirm</span></span>
<span data-ttu-id="3574d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3574d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3574d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3574d-123">-WhatIf</span></span>
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

### <span data-ttu-id="3574d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3574d-124">CommonParameters</span></span>
<span data-ttu-id="3574d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3574d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3574d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3574d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3574d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3574d-127">INPUTS</span></span>

### <span data-ttu-id="3574d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3574d-128">System.String</span></span>

## <span data-ttu-id="3574d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3574d-129">OUTPUTS</span></span>

### <span data-ttu-id="3574d-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3574d-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3574d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3574d-131">NOTES</span></span>

## <span data-ttu-id="3574d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3574d-132">RELATED LINKS</span></span>