---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758063"
---
# <span data-ttu-id="b9222-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b9222-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="b9222-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9222-102">SYNOPSIS</span></span>
<span data-ttu-id="b9222-103">Skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b9222-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9222-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9222-104">SYNTAX</span></span>

### <span data-ttu-id="b9222-105">Parametrar för Add-AzureRmAutoscaleSetting cmdlet i uppdateringens semantik</span><span class="sxs-lookup"><span data-stu-id="b9222-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9222-106">Parametrar för Add-AzureRmAutoscaleSetting cmdlet i Create semantik</span><span class="sxs-lookup"><span data-stu-id="b9222-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9222-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9222-107">DESCRIPTION</span></span>
<span data-ttu-id="b9222-108">Cmdleten **Add-AzureRmAutoscaleSetting** skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b9222-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="b9222-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9222-109">EXAMPLES</span></span>

### <span data-ttu-id="b9222-110">Exempel 1: skapa en autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="b9222-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="b9222-111">De två första kommandona använder New-AzureRmAutoscaleRule för att skapa två Autoskala-regler, $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="b9222-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="b9222-112">De tredje och fjärde kommandona använder New-AzureRmAutoscaleProfile för att skapa Autoskala-profiler, $Profile 1 och $Profile 2, med $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="b9222-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="b9222-113">Med kommandot slut skapas en inställning för autoskalningsinställning med hjälp av profilerna i $Profile 1 och $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="b9222-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="b9222-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9222-114">PARAMETERS</span></span>

### <span data-ttu-id="b9222-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="b9222-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="b9222-116">Anger en lista med profiler som ska läggas till i den autoskalningsinställning eller $Null att ingen profil ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b9222-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="b9222-117">-DisableSetting</span></span>
<span data-ttu-id="b9222-118">Inaktiverar en befintlig autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b9222-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="b9222-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="b9222-119">-Location</span></span>
<span data-ttu-id="b9222-120">Anger platsen för den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b9222-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9222-121">-Name</span></span>
<span data-ttu-id="b9222-122">Anger namnet på den autoskalningsinställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b9222-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-123">-Meddelanden</span><span class="sxs-lookup"><span data-stu-id="b9222-123">-Notifications</span></span>
<span data-ttu-id="b9222-124">Anger en lista med kommaavgränsade meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b9222-124">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9222-125">-ResourceGroup</span></span>
<span data-ttu-id="b9222-126">Anger namnet på resurs gruppen för resursen som är associerad med den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b9222-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="b9222-127">-SettingSpec</span></span>
<span data-ttu-id="b9222-128">Anger ett **AutoscaleSetting** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b9222-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="b9222-129">Du kan använda Get-AzureRmAutoscaleSetting cmdlet för att få ett **AutoscaleSetting** -objekt eller skapa ett i ett Windows PowerShell-skript.</span><span class="sxs-lookup"><span data-stu-id="b9222-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b9222-130">-TargetResourceId</span></span>
<span data-ttu-id="b9222-131">Anger ID för resursen till Autoskala.</span><span class="sxs-lookup"><span data-stu-id="b9222-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9222-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9222-132">-DefaultProfile</span></span>
<span data-ttu-id="b9222-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9222-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9222-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9222-134">CommonParameters</span></span>
<span data-ttu-id="b9222-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9222-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9222-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9222-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9222-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9222-137">INPUTS</span></span>

## <span data-ttu-id="b9222-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9222-138">OUTPUTS</span></span>

### <span data-ttu-id="b9222-139">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b9222-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="b9222-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9222-140">NOTES</span></span>

## <span data-ttu-id="b9222-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9222-141">RELATED LINKS</span></span>

[<span data-ttu-id="b9222-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b9222-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b9222-143">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b9222-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="b9222-144">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b9222-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="b9222-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b9222-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


