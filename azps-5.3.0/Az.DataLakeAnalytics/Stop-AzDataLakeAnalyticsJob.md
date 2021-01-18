---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526157"
---
# <span data-ttu-id="01e51-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01e51-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="01e51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01e51-102">SYNOPSIS</span></span>
<span data-ttu-id="01e51-103">Avbryter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="01e51-103">Cancels a job.</span></span>

## <span data-ttu-id="01e51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01e51-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01e51-105">DESCRIPTION</span></span>
<span data-ttu-id="01e51-106">Cmdleten **Stop-AzDataLakeAnalyticsJob** avbryter ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="01e51-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="01e51-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01e51-107">EXAMPLES</span></span>

### <span data-ttu-id="01e51-108">Exempel 1: avbryta ett jobb</span><span class="sxs-lookup"><span data-stu-id="01e51-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="01e51-109">Det här kommandot avbryter jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="01e51-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="01e51-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01e51-110">PARAMETERS</span></span>

### <span data-ttu-id="01e51-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="01e51-111">-Account</span></span>
<span data-ttu-id="01e51-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="01e51-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="01e51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e51-113">-DefaultProfile</span></span>
<span data-ttu-id="01e51-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="01e51-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01e51-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01e51-115">-Force</span></span>
<span data-ttu-id="01e51-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="01e51-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01e51-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="01e51-117">-JobId</span></span>
<span data-ttu-id="01e51-118">Anger ID för jobbet som ska avbrytas.</span><span class="sxs-lookup"><span data-stu-id="01e51-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="01e51-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e51-119">-PassThru</span></span>
<span data-ttu-id="01e51-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="01e51-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01e51-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="01e51-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01e51-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01e51-122">-Confirm</span></span>
<span data-ttu-id="01e51-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01e51-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e51-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e51-124">-WhatIf</span></span>
<span data-ttu-id="01e51-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01e51-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e51-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01e51-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e51-127">CommonParameters</span></span>
<span data-ttu-id="01e51-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e51-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e51-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e51-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01e51-130">INPUTS</span></span>

### <span data-ttu-id="01e51-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01e51-131">System.String</span></span>

### <span data-ttu-id="01e51-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="01e51-132">System.Guid</span></span>

### <span data-ttu-id="01e51-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="01e51-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="01e51-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01e51-134">OUTPUTS</span></span>

### <span data-ttu-id="01e51-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01e51-135">System.Boolean</span></span>

## <span data-ttu-id="01e51-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01e51-136">NOTES</span></span>

## <span data-ttu-id="01e51-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01e51-137">RELATED LINKS</span></span>

[<span data-ttu-id="01e51-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01e51-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="01e51-139">Skicka-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01e51-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="01e51-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01e51-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


