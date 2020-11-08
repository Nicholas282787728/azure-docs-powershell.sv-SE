---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088556"
---
# <span data-ttu-id="2a800-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="2a800-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="2a800-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a800-102">SYNOPSIS</span></span>
<span data-ttu-id="2a800-103">Tar bort ett Azure Data Lake Analytics-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="2a800-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="2a800-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a800-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a800-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a800-105">DESCRIPTION</span></span>
<span data-ttu-id="2a800-106">Remove-AzDataLakeAnalyticsCatalogCredential-cmdleten tar bort en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="2a800-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="2a800-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a800-107">EXAMPLES</span></span>

### <span data-ttu-id="2a800-108">Exempel 1: ta bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="2a800-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="2a800-109">Detta kommando tar bort den angivna autentiseringsuppgiften för data Lake-katalog.</span><span class="sxs-lookup"><span data-stu-id="2a800-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="2a800-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a800-110">PARAMETERS</span></span>

### <span data-ttu-id="2a800-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2a800-111">-Account</span></span>
<span data-ttu-id="2a800-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="2a800-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2a800-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a800-113">-DatabaseName</span></span>
<span data-ttu-id="2a800-114">Anger namnet på den databas som innehåller autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="2a800-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="2a800-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a800-115">-DefaultProfile</span></span>
<span data-ttu-id="2a800-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2a800-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a800-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2a800-117">-Force</span></span>
<span data-ttu-id="2a800-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2a800-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a800-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a800-119">-Name</span></span>
<span data-ttu-id="2a800-120">Anger namnet på autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="2a800-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="2a800-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a800-121">-PassThru</span></span>
<span data-ttu-id="2a800-122">Anger att denna cmdlet inte väntar på att åtgärden ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="2a800-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="2a800-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2a800-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a800-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2a800-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a800-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="2a800-125">-Password</span></span>
<span data-ttu-id="2a800-126">Lösen ordet för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="2a800-126">The password for the credential.</span></span>
<span data-ttu-id="2a800-127">Det här är obligatoriskt om den som ringer inte är ägare till kontot.</span><span class="sxs-lookup"><span data-stu-id="2a800-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="2a800-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="2a800-128">-Recurse</span></span>
<span data-ttu-id="2a800-129">Anger att den här borttagnings åtgärden ska gå igenom och även ta bort och släppa alla resurser som är beroende av den här autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="2a800-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="2a800-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a800-130">-Confirm</span></span>
<span data-ttu-id="2a800-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a800-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a800-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a800-132">-WhatIf</span></span>
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

### <span data-ttu-id="2a800-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a800-133">CommonParameters</span></span>
<span data-ttu-id="2a800-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a800-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a800-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a800-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a800-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a800-136">INPUTS</span></span>

### <span data-ttu-id="2a800-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2a800-137">System.String</span></span>

### <span data-ttu-id="2a800-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2a800-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="2a800-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a800-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a800-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a800-140">OUTPUTS</span></span>

### <span data-ttu-id="2a800-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a800-141">System.Boolean</span></span>

## <span data-ttu-id="2a800-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a800-142">NOTES</span></span>

## <span data-ttu-id="2a800-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a800-143">RELATED LINKS</span></span>