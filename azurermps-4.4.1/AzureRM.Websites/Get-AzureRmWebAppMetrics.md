---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 00e8814c72f0e9d52fae2504a41bef3e8e94e7ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756300"
---
# <span data-ttu-id="f425b-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="f425b-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="f425b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f425b-102">SYNOPSIS</span></span>
<span data-ttu-id="f425b-103">Hämtar Azure Web App-mått.</span><span class="sxs-lookup"><span data-stu-id="f425b-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f425b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f425b-104">SYNTAX</span></span>

### <span data-ttu-id="f425b-105">S</span><span class="sxs-lookup"><span data-stu-id="f425b-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f425b-106">S2</span><span class="sxs-lookup"><span data-stu-id="f425b-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f425b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f425b-107">DESCRIPTION</span></span>
<span data-ttu-id="f425b-108">**Get-AzureRmWebAppMetrics** får webb program mått.</span><span class="sxs-lookup"><span data-stu-id="f425b-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="f425b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f425b-109">EXAMPLES</span></span>

### <span data-ttu-id="f425b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f425b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="f425b-111">Det här kommandot får begäran från webb programmet ContosoWebApp per minut (PT1M-omröstning Time 1 minut) mellan start tid och slut tid</span><span class="sxs-lookup"><span data-stu-id="f425b-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="f425b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f425b-112">PARAMETERS</span></span>

### <span data-ttu-id="f425b-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="f425b-113">-EndTime</span></span>
<span data-ttu-id="f425b-114">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="f425b-114">End Time in UTC</span></span>

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

### <span data-ttu-id="f425b-115">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="f425b-115">-Granularity</span></span>
<span data-ttu-id="f425b-116">Granularitet</span><span class="sxs-lookup"><span data-stu-id="f425b-116">Granularity</span></span>

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

### <span data-ttu-id="f425b-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="f425b-117">-InstanceDetails</span></span>
<span data-ttu-id="f425b-118">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="f425b-118">Instance Details</span></span>

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

### <span data-ttu-id="f425b-119">-Mått</span><span class="sxs-lookup"><span data-stu-id="f425b-119">-Metrics</span></span>
<span data-ttu-id="f425b-120">Mått som en sträng mat ris</span><span class="sxs-lookup"><span data-stu-id="f425b-120">Metrics as a string array</span></span>

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

### <span data-ttu-id="f425b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f425b-121">-Name</span></span>
<span data-ttu-id="f425b-122">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="f425b-122">WebApp Name</span></span>

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

### <span data-ttu-id="f425b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f425b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f425b-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f425b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f425b-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f425b-125">-StartTime</span></span>
<span data-ttu-id="f425b-126">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="f425b-126">Start Time in UTC</span></span>

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

### <span data-ttu-id="f425b-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f425b-127">-WebApp</span></span>
<span data-ttu-id="f425b-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="f425b-128">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f425b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f425b-129">-DefaultProfile</span></span>
<span data-ttu-id="f425b-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f425b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f425b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f425b-131">CommonParameters</span></span>
<span data-ttu-id="f425b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f425b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f425b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f425b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f425b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f425b-134">INPUTS</span></span>

### <span data-ttu-id="f425b-135">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="f425b-135">Site</span></span>
<span data-ttu-id="f425b-136">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f425b-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f425b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f425b-137">OUTPUTS</span></span>

## <span data-ttu-id="f425b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f425b-138">NOTES</span></span>

## <span data-ttu-id="f425b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f425b-139">RELATED LINKS</span></span>

[<span data-ttu-id="f425b-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f425b-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

