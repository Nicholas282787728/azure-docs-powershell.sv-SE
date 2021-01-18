---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522550"
---
# <span data-ttu-id="2bc2b-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="2bc2b-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="2bc2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc2b-103">Skapa PSDiagnosticDetailSetting-objekt, typ kan vara metriskt eller log</span><span class="sxs-lookup"><span data-stu-id="2bc2b-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="2bc2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc2b-104">SYNTAX</span></span>

### <span data-ttu-id="2bc2b-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bc2b-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bc2b-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bc2b-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc2b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc2b-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc2b-108">Skapa PSMetricSettings-eller PSLogSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="2bc2b-109">Du kan få kategorier genom att använda `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="2bc2b-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="2bc2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc2b-110">EXAMPLES</span></span>

### <span data-ttu-id="2bc2b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bc2b-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="2bc2b-112">Skapa PSMetricSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="2bc2b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2bc2b-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="2bc2b-114">Skapa PSLogSettings-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="2bc2b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc2b-115">PARAMETERS</span></span>

### <span data-ttu-id="2bc2b-116">-Kategori</span><span class="sxs-lookup"><span data-stu-id="2bc2b-116">-Category</span></span>
<span data-ttu-id="2bc2b-117">Inställnings kategori</span><span class="sxs-lookup"><span data-stu-id="2bc2b-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc2b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc2b-118">-DefaultProfile</span></span>
<span data-ttu-id="2bc2b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc2b-120">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="2bc2b-120">-Enabled</span></span>
<span data-ttu-id="2bc2b-121">Aktivera inställningen</span><span class="sxs-lookup"><span data-stu-id="2bc2b-121">Enable the setting</span></span>

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

### <span data-ttu-id="2bc2b-122">-Logga in</span><span class="sxs-lookup"><span data-stu-id="2bc2b-122">-Log</span></span>
<span data-ttu-id="2bc2b-123">Så här skapar du logg inställning</span><span class="sxs-lookup"><span data-stu-id="2bc2b-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc2b-124">-Metrisk</span><span class="sxs-lookup"><span data-stu-id="2bc2b-124">-Metric</span></span>
<span data-ttu-id="2bc2b-125">Skapa mått inställningar</span><span class="sxs-lookup"><span data-stu-id="2bc2b-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc2b-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="2bc2b-126">-RetentionEnabled</span></span>
<span data-ttu-id="2bc2b-127">Aktivera bevarande princip</span><span class="sxs-lookup"><span data-stu-id="2bc2b-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="2bc2b-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2bc2b-128">-RetentionInDays</span></span>
<span data-ttu-id="2bc2b-129">Bevarande dagar för bevarande princip</span><span class="sxs-lookup"><span data-stu-id="2bc2b-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc2b-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2bc2b-130">-TimeGrain</span></span>
<span data-ttu-id="2bc2b-131">TimeGrain för mått inställning</span><span class="sxs-lookup"><span data-stu-id="2bc2b-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc2b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc2b-132">CommonParameters</span></span>
<span data-ttu-id="2bc2b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc2b-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bc2b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc2b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc2b-135">INPUTS</span></span>

### <span data-ttu-id="2bc2b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc2b-136">System.String</span></span>

## <span data-ttu-id="2bc2b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc2b-137">OUTPUTS</span></span>

### <span data-ttu-id="2bc2b-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="2bc2b-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="2bc2b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc2b-139">NOTES</span></span>

## <span data-ttu-id="2bc2b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc2b-140">RELATED LINKS</span></span>
