---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 4fc5c20cf43fbafb89007328307c69d4820b2127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756192"
---
# <span data-ttu-id="c2987-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c2987-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="c2987-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2987-102">SYNOPSIS</span></span>
<span data-ttu-id="c2987-103">Avbryter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="c2987-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2987-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2987-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2987-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2987-105">DESCRIPTION</span></span>
<span data-ttu-id="c2987-106">Cmdleten **Stop-AzureRmDataLakeAnalyticsJob** avbryter ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="c2987-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="c2987-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2987-107">EXAMPLES</span></span>

### <span data-ttu-id="c2987-108">Exempel 1: avbryta ett jobb</span><span class="sxs-lookup"><span data-stu-id="c2987-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="c2987-109">Det här kommandot avbryter jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="c2987-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="c2987-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2987-110">PARAMETERS</span></span>

### <span data-ttu-id="c2987-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="c2987-111">-Account</span></span>
<span data-ttu-id="c2987-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="c2987-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c2987-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2987-113">-DefaultProfile</span></span>
<span data-ttu-id="c2987-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c2987-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2987-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c2987-115">-Force</span></span>
<span data-ttu-id="c2987-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c2987-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2987-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c2987-117">-JobId</span></span>
<span data-ttu-id="c2987-118">Anger ID för jobbet som ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="c2987-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2987-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2987-119">-PassThru</span></span>
<span data-ttu-id="c2987-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c2987-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2987-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c2987-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2987-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2987-122">-Confirm</span></span>
<span data-ttu-id="c2987-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2987-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2987-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2987-124">-WhatIf</span></span>
<span data-ttu-id="c2987-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2987-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2987-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2987-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2987-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2987-127">CommonParameters</span></span>
<span data-ttu-id="c2987-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2987-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2987-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2987-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2987-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2987-130">INPUTS</span></span>

### <span data-ttu-id="c2987-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c2987-131">System.String</span></span>

### <span data-ttu-id="c2987-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c2987-132">System.Guid</span></span>

### <span data-ttu-id="c2987-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2987-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2987-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2987-134">OUTPUTS</span></span>

### <span data-ttu-id="c2987-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2987-135">System.Boolean</span></span>

## <span data-ttu-id="c2987-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2987-136">NOTES</span></span>

## <span data-ttu-id="c2987-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2987-137">RELATED LINKS</span></span>

[<span data-ttu-id="c2987-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c2987-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c2987-139">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c2987-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c2987-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c2987-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


