---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 604eec977e8cb821986e3dcc0690fa4dfb65b526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921134"
---
# <span data-ttu-id="d7bcd-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="d7bcd-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="d7bcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bcd-103">Hämtar Azure Web App-mått.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="d7bcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7bcd-104">SYNTAX</span></span>

### <span data-ttu-id="d7bcd-105">S</span><span class="sxs-lookup"><span data-stu-id="d7bcd-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bcd-106">S2</span><span class="sxs-lookup"><span data-stu-id="d7bcd-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7bcd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="d7bcd-108">**Get-AzWebAppMetric** får webb program mått.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="d7bcd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7bcd-109">EXAMPLES</span></span>

### <span data-ttu-id="d7bcd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d7bcd-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="d7bcd-111">Det här kommandot får begäran från webb programmet ContosoWebApp per minut (PT1M-omröstning Time 1 minut) mellan start tid och slut tid</span><span class="sxs-lookup"><span data-stu-id="d7bcd-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="d7bcd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7bcd-112">PARAMETERS</span></span>

### <span data-ttu-id="d7bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="d7bcd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7bcd-115">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="d7bcd-115">-EndTime</span></span>
<span data-ttu-id="d7bcd-116">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="d7bcd-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-117">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="d7bcd-117">-Granularity</span></span>
<span data-ttu-id="d7bcd-118">Granularitet</span><span class="sxs-lookup"><span data-stu-id="d7bcd-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="d7bcd-119">-InstanceDetails</span></span>
<span data-ttu-id="d7bcd-120">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="d7bcd-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-121">-Mått</span><span class="sxs-lookup"><span data-stu-id="d7bcd-121">-Metrics</span></span>
<span data-ttu-id="d7bcd-122">Mått som en sträng mat ris</span><span class="sxs-lookup"><span data-stu-id="d7bcd-122">Metrics as a string array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7bcd-123">-Name</span></span>
<span data-ttu-id="d7bcd-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d7bcd-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bcd-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7bcd-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d7bcd-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d7bcd-127">-StartTime</span></span>
<span data-ttu-id="d7bcd-128">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="d7bcd-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d7bcd-129">-WebApp</span></span>
<span data-ttu-id="d7bcd-130">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d7bcd-130">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bcd-131">CommonParameters</span></span>
<span data-ttu-id="d7bcd-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bcd-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7bcd-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bcd-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7bcd-134">INPUTS</span></span>

### <span data-ttu-id="d7bcd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bcd-135">System.String</span></span>

### <span data-ttu-id="d7bcd-136">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d7bcd-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d7bcd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7bcd-137">OUTPUTS</span></span>

### <span data-ttu-id="d7bcd-138">Microsoft. Azure. Management. webbplatser. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="d7bcd-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="d7bcd-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7bcd-139">NOTES</span></span>

## <span data-ttu-id="d7bcd-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7bcd-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7bcd-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d7bcd-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

