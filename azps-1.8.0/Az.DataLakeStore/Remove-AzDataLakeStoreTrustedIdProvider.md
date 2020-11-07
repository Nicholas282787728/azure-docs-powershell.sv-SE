---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a93eb93a02c0ba1f5654258da0405f723e69873d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754285"
---
# <span data-ttu-id="abaa0-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="abaa0-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="abaa0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="abaa0-103">Tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abaa0-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="abaa0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abaa0-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abaa0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abaa0-105">DESCRIPTION</span></span>
<span data-ttu-id="abaa0-106">Cmdleten **Remove-AzDataLakeStoreTrustedIdProvider** tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abaa0-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="abaa0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abaa0-107">EXAMPLES</span></span>

### <span data-ttu-id="abaa0-108">Exempel 1: ta bort en betrodd identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="abaa0-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="abaa0-109">Tar bort leverantören "" "leverantör" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="abaa0-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="abaa0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abaa0-110">PARAMETERS</span></span>

### <span data-ttu-id="abaa0-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="abaa0-111">-Account</span></span>
<span data-ttu-id="abaa0-112">Data Lake Store-kontot för att ta bort den betrodda identitets leverantören från</span><span class="sxs-lookup"><span data-stu-id="abaa0-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="abaa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abaa0-113">-DefaultProfile</span></span>
<span data-ttu-id="abaa0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="abaa0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abaa0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="abaa0-115">-Name</span></span>
<span data-ttu-id="abaa0-116">Namnet på den betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="abaa0-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="abaa0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abaa0-117">-PassThru</span></span>
<span data-ttu-id="abaa0-118">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="abaa0-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="abaa0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abaa0-119">-ResourceGroupName</span></span>
<span data-ttu-id="abaa0-120">Anger namnet på den resurs grupp som innehåller kontot som den betrodda identitets leverantören ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="abaa0-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="abaa0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abaa0-121">-Confirm</span></span>
<span data-ttu-id="abaa0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abaa0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abaa0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abaa0-123">-WhatIf</span></span>
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

### <span data-ttu-id="abaa0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abaa0-124">CommonParameters</span></span>
<span data-ttu-id="abaa0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abaa0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abaa0-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abaa0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abaa0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abaa0-127">INPUTS</span></span>

### <span data-ttu-id="abaa0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="abaa0-128">System.String</span></span>

### <span data-ttu-id="abaa0-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="abaa0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="abaa0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abaa0-130">OUTPUTS</span></span>

### <span data-ttu-id="abaa0-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abaa0-131">System.Boolean</span></span>

## <span data-ttu-id="abaa0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abaa0-132">NOTES</span></span>

## <span data-ttu-id="abaa0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abaa0-133">RELATED LINKS</span></span>