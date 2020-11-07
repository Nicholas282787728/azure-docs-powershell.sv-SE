---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: aa7dace3141210e8c4ff6055a011f34523c5b586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575236"
---
# <span data-ttu-id="fb4bb-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb4bb-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="fb4bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4bb-103">Tar bort en hemlighet för data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb4bb-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4bb-106">Cmdleten **Remove-AzureRmDataLakeAnalyticsCatalogSecret** tar bort en Azure Data Lake Analytics-katalog hemlighet.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="fb4bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4bb-108">Exempel 1: ta bort en hemlighet</span><span class="sxs-lookup"><span data-stu-id="fb4bb-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="fb4bb-109">Det här kommandot tar bort den angivna data Lake-katalog hemligheten.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="fb4bb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="fb4bb-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="fb4bb-111">-Account</span></span>
<span data-ttu-id="fb4bb-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fb4bb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb4bb-113">-DatabaseName</span></span>
<span data-ttu-id="fb4bb-114">Anger namnet på den databas som innehåller hemligheten.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="fb4bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4bb-115">-DefaultProfile</span></span>
<span data-ttu-id="fb4bb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb4bb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb4bb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb4bb-117">-Force</span></span>
<span data-ttu-id="fb4bb-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb4bb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb4bb-119">-Name</span></span>
<span data-ttu-id="fb4bb-120">Anger namnet på hemligheten.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-120">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="fb4bb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb4bb-121">-PassThru</span></span>
<span data-ttu-id="fb4bb-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb4bb-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb4bb-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb4bb-124">-Confirm</span></span>
<span data-ttu-id="fb4bb-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4bb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4bb-126">-WhatIf</span></span>
<span data-ttu-id="fb4bb-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb4bb-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4bb-129">CommonParameters</span></span>
<span data-ttu-id="fb4bb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4bb-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4bb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb4bb-132">INPUTS</span></span>

### <span data-ttu-id="fb4bb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4bb-133">System.String</span></span>

## <span data-ttu-id="fb4bb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb4bb-134">OUTPUTS</span></span>

### <span data-ttu-id="fb4bb-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb4bb-135">System.Boolean</span></span>

## <span data-ttu-id="fb4bb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb4bb-136">NOTES</span></span>

## <span data-ttu-id="fb4bb-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb4bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb4bb-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb4bb-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="fb4bb-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="fb4bb-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)

