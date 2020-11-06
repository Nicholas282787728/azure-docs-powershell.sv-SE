---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574691"
---
# <span data-ttu-id="80844-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="80844-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="80844-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80844-102">SYNOPSIS</span></span>
<span data-ttu-id="80844-103">Tar bort ett Azure Data Lake Analytics-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="80844-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80844-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80844-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80844-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80844-105">DESCRIPTION</span></span>
<span data-ttu-id="80844-106">Remove-AzureRmDataLakeAnalyticsCatalogCredential-cmdleten tar bort en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="80844-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="80844-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80844-107">EXAMPLES</span></span>

### <span data-ttu-id="80844-108">Exempel 1: ta bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="80844-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="80844-109">Detta kommando tar bort den angivna autentiseringsuppgiften för data Lake-katalog.</span><span class="sxs-lookup"><span data-stu-id="80844-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="80844-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80844-110">PARAMETERS</span></span>

### <span data-ttu-id="80844-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="80844-111">-Account</span></span>
<span data-ttu-id="80844-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="80844-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="80844-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80844-113">-DatabaseName</span></span>
<span data-ttu-id="80844-114">Anger namnet på den databas som innehåller autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="80844-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="80844-115">-Force</span><span class="sxs-lookup"><span data-stu-id="80844-115">-Force</span></span>
<span data-ttu-id="80844-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="80844-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80844-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="80844-117">-Name</span></span>
<span data-ttu-id="80844-118">Anger namnet på autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="80844-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="80844-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80844-119">-PassThru</span></span>
<span data-ttu-id="80844-120">Anger att denna cmdlet inte väntar på att åtgärden ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="80844-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="80844-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="80844-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="80844-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="80844-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80844-123">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="80844-123">-Password</span></span>
<span data-ttu-id="80844-124">Lösen ordet för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="80844-124">The password for the credential.</span></span>
<span data-ttu-id="80844-125">Det här är obligatoriskt om den som ringer inte är ägare till kontot.</span><span class="sxs-lookup"><span data-stu-id="80844-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80844-126">-Recurse</span><span class="sxs-lookup"><span data-stu-id="80844-126">-Recurse</span></span>
<span data-ttu-id="80844-127">Anger att den här borttagnings åtgärden ska gå igenom och även ta bort och släppa alla resurser som är beroende av den här autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="80844-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="80844-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80844-128">-Confirm</span></span>
<span data-ttu-id="80844-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80844-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80844-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80844-130">-WhatIf</span></span>
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

### <span data-ttu-id="80844-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80844-131">-DefaultProfile</span></span>
<span data-ttu-id="80844-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80844-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80844-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80844-133">CommonParameters</span></span>
<span data-ttu-id="80844-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80844-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80844-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80844-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80844-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80844-136">INPUTS</span></span>

## <span data-ttu-id="80844-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80844-137">OUTPUTS</span></span>

### <span data-ttu-id="80844-138">bool</span><span class="sxs-lookup"><span data-stu-id="80844-138">bool</span></span>
<span data-ttu-id="80844-139">Om PassThru anges returneras sant när åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="80844-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="80844-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80844-140">NOTES</span></span>

## <span data-ttu-id="80844-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80844-141">RELATED LINKS</span></span>

