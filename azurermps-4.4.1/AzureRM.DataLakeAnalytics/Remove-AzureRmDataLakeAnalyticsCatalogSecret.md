---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757003"
---
# <span data-ttu-id="161c9-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="161c9-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="161c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="161c9-102">SYNOPSIS</span></span>
<span data-ttu-id="161c9-103">Tar bort en hemlighet för data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="161c9-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="161c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="161c9-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="161c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="161c9-105">DESCRIPTION</span></span>
<span data-ttu-id="161c9-106">Cmdleten **Remove-AzureRmDataLakeAnalyticsCatalogSecret** tar bort en Azure Data Lake Analytics-katalog hemlighet.</span><span class="sxs-lookup"><span data-stu-id="161c9-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="161c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="161c9-107">EXAMPLES</span></span>

### <span data-ttu-id="161c9-108">Exempel 1: ta bort en hemlighet</span><span class="sxs-lookup"><span data-stu-id="161c9-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="161c9-109">Det här kommandot tar bort den angivna data Lake-katalog hemligheten.</span><span class="sxs-lookup"><span data-stu-id="161c9-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="161c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="161c9-110">PARAMETERS</span></span>

### <span data-ttu-id="161c9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="161c9-111">-Account</span></span>
<span data-ttu-id="161c9-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="161c9-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="161c9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="161c9-113">-DatabaseName</span></span>
<span data-ttu-id="161c9-114">Anger namnet på den databas som innehåller hemligheten.</span><span class="sxs-lookup"><span data-stu-id="161c9-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="161c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="161c9-115">-Force</span></span>
<span data-ttu-id="161c9-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="161c9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161c9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="161c9-117">-Name</span></span>
<span data-ttu-id="161c9-118">Anger namnet på hemligheten.</span><span class="sxs-lookup"><span data-stu-id="161c9-118">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="161c9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="161c9-119">-PassThru</span></span>
<span data-ttu-id="161c9-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="161c9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="161c9-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="161c9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161c9-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="161c9-122">-Confirm</span></span>
<span data-ttu-id="161c9-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="161c9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161c9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="161c9-124">-WhatIf</span></span>
<span data-ttu-id="161c9-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="161c9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="161c9-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="161c9-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161c9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161c9-127">-DefaultProfile</span></span>
<span data-ttu-id="161c9-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="161c9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="161c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161c9-129">CommonParameters</span></span>
<span data-ttu-id="161c9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="161c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161c9-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="161c9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161c9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="161c9-132">INPUTS</span></span>

## <span data-ttu-id="161c9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="161c9-133">OUTPUTS</span></span>

### <span data-ttu-id="161c9-134">bool</span><span class="sxs-lookup"><span data-stu-id="161c9-134">bool</span></span>
<span data-ttu-id="161c9-135">Om PassThru anges returneras sant när åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="161c9-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="161c9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="161c9-136">NOTES</span></span>

## <span data-ttu-id="161c9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="161c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="161c9-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="161c9-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="161c9-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="161c9-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


