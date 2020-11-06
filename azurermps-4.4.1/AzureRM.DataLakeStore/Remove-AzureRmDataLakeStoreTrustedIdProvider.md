---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 089dbc5e3ca1d6a4a2a6528cb0c4bc87cf9b3dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586540"
---
# <span data-ttu-id="24371-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="24371-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="24371-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24371-102">SYNOPSIS</span></span>
<span data-ttu-id="24371-103">Tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24371-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24371-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24371-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24371-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24371-105">DESCRIPTION</span></span>
<span data-ttu-id="24371-106">Cmdleten **Remove-AzureRmDataLakeStoreTrustedIdProvider** tar bort den angivna betrodda identitets leverantören i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24371-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="24371-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24371-107">EXAMPLES</span></span>

### <span data-ttu-id="24371-108">Exempel 1: ta bort en betrodd identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="24371-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="24371-109">Tar bort leverantören "" "leverantör" från kontot "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="24371-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="24371-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24371-110">PARAMETERS</span></span>

### <span data-ttu-id="24371-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="24371-111">-Account</span></span>
<span data-ttu-id="24371-112">Data Lake Store-kontot för att ta bort den betrodda identitets leverantören från</span><span class="sxs-lookup"><span data-stu-id="24371-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="24371-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="24371-113">-Name</span></span>
<span data-ttu-id="24371-114">Namnet på den betrodda identitets leverantören.</span><span class="sxs-lookup"><span data-stu-id="24371-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="24371-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24371-115">-PassThru</span></span>
<span data-ttu-id="24371-116">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="24371-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="24371-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24371-117">-ResourceGroupName</span></span>
<span data-ttu-id="24371-118">Anger namnet på den resurs grupp som innehåller kontot som den betrodda identitets leverantören ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="24371-118">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="24371-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24371-119">-Confirm</span></span>
<span data-ttu-id="24371-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24371-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24371-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24371-121">-WhatIf</span></span>
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

### <span data-ttu-id="24371-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24371-122">-DefaultProfile</span></span>
<span data-ttu-id="24371-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24371-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24371-124">CommonParameters</span></span>
<span data-ttu-id="24371-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24371-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24371-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24371-127">INPUTS</span></span>

## <span data-ttu-id="24371-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24371-128">OUTPUTS</span></span>

### <span data-ttu-id="24371-129">bool</span><span class="sxs-lookup"><span data-stu-id="24371-129">bool</span></span>
<span data-ttu-id="24371-130">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="24371-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="24371-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24371-131">NOTES</span></span>

## <span data-ttu-id="24371-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24371-132">RELATED LINKS</span></span>

