---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260240"
---
# <span data-ttu-id="44cdc-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="44cdc-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="44cdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="44cdc-103">Tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44cdc-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="44cdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44cdc-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44cdc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="44cdc-106">Cmdleten **Remove-AzDataLakeStoreTrustedIdProvider** tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44cdc-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="44cdc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="44cdc-108">Exempel 1: ta bort en betrodd identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="44cdc-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="44cdc-109">Tar bort leverantören "" "leverantör" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="44cdc-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="44cdc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="44cdc-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="44cdc-111">-Account</span></span>
<span data-ttu-id="44cdc-112">Data Lake Store-kontot för att ta bort den betrodda identitets leverantören från</span><span class="sxs-lookup"><span data-stu-id="44cdc-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="44cdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cdc-113">-DefaultProfile</span></span>
<span data-ttu-id="44cdc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="44cdc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44cdc-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="44cdc-115">-Name</span></span>
<span data-ttu-id="44cdc-116">Namnet på den betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="44cdc-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="44cdc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44cdc-117">-PassThru</span></span>
<span data-ttu-id="44cdc-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="44cdc-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="44cdc-120">Anger namnet på den resurs grupp som innehåller kontot som den betrodda identitets leverantören ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="44cdc-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cdc-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44cdc-121">-Confirm</span></span>
<span data-ttu-id="44cdc-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44cdc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cdc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cdc-123">-WhatIf</span></span>
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

### <span data-ttu-id="44cdc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cdc-124">CommonParameters</span></span>
<span data-ttu-id="44cdc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cdc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cdc-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cdc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cdc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44cdc-127">INPUTS</span></span>

### <span data-ttu-id="44cdc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44cdc-128">System.String</span></span>

### <span data-ttu-id="44cdc-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="44cdc-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44cdc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44cdc-130">OUTPUTS</span></span>

### <span data-ttu-id="44cdc-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44cdc-131">System.Boolean</span></span>

## <span data-ttu-id="44cdc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44cdc-132">NOTES</span></span>

## <span data-ttu-id="44cdc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44cdc-133">RELATED LINKS</span></span>
