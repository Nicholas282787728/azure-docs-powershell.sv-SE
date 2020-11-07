---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757795"
---
# <span data-ttu-id="cc779-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cc779-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="cc779-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc779-102">SYNOPSIS</span></span>
<span data-ttu-id="cc779-103">Avbryter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="cc779-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc779-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc779-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc779-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc779-105">DESCRIPTION</span></span>
<span data-ttu-id="cc779-106">Cmdleten **Stop-AzureRmDataLakeAnalyticsJob** avbryter ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="cc779-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="cc779-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc779-107">EXAMPLES</span></span>

### <span data-ttu-id="cc779-108">Exempel 1: avbryta ett jobb</span><span class="sxs-lookup"><span data-stu-id="cc779-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="cc779-109">Det här kommandot avbryter jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="cc779-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="cc779-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc779-110">PARAMETERS</span></span>

### <span data-ttu-id="cc779-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="cc779-111">-Account</span></span>
<span data-ttu-id="cc779-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="cc779-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cc779-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cc779-113">-Force</span></span>
<span data-ttu-id="cc779-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cc779-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc779-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="cc779-115">-JobId</span></span>
<span data-ttu-id="cc779-116">Anger ID för jobbet som ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="cc779-116">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="cc779-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc779-117">-PassThru</span></span>
<span data-ttu-id="cc779-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="cc779-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc779-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cc779-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc779-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc779-120">-Confirm</span></span>
<span data-ttu-id="cc779-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc779-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc779-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc779-122">-WhatIf</span></span>
<span data-ttu-id="cc779-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc779-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc779-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc779-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc779-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc779-125">-DefaultProfile</span></span>
<span data-ttu-id="cc779-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc779-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc779-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc779-127">CommonParameters</span></span>
<span data-ttu-id="cc779-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc779-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc779-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc779-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc779-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc779-130">INPUTS</span></span>

### <span data-ttu-id="cc779-131">Ande</span><span class="sxs-lookup"><span data-stu-id="cc779-131">Guid</span></span>
<span data-ttu-id="cc779-132">Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cc779-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="cc779-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc779-133">OUTPUTS</span></span>

### <span data-ttu-id="cc779-134">bool</span><span class="sxs-lookup"><span data-stu-id="cc779-134">bool</span></span>
<span data-ttu-id="cc779-135">Om PassThru anges returneras sant när åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="cc779-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="cc779-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc779-136">NOTES</span></span>

## <span data-ttu-id="cc779-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc779-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc779-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cc779-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="cc779-139">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cc779-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="cc779-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cc779-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


