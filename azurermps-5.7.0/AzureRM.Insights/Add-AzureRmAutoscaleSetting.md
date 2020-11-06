---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585140"
---
# <span data-ttu-id="c34a1-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="c34a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c34a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c34a1-103">Skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="c34a1-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c34a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c34a1-104">SYNTAX</span></span>

### <span data-ttu-id="c34a1-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c34a1-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c34a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c34a1-108">Cmdleten **Add-AzureRmAutoscaleSetting** skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="c34a1-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

<span data-ttu-id="c34a1-109">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="c34a1-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c34a1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c34a1-110">EXAMPLES</span></span>

### <span data-ttu-id="c34a1-111">Exempel 1: skapa en autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="c34a1-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="c34a1-112">De två första kommandona använder New-AzureRmAutoscaleRule för att skapa två Autoskala-regler, $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c34a1-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="c34a1-113">De tredje och fjärde kommandona använder New-AzureRmAutoscaleProfile för att skapa Autoskala-profiler, $Profile 1 och $Profile 2, med $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c34a1-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="c34a1-114">Med kommandot slut skapas en inställning för autoskalningsinställning med hjälp av profilerna i $Profile 1 och $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="c34a1-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="c34a1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c34a1-115">PARAMETERS</span></span>

### <span data-ttu-id="c34a1-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c34a1-116">-AutoscaleProfile</span></span>
<span data-ttu-id="c34a1-117">Anger en lista med profiler som ska läggas till i den autoskalningsinställning eller $Null att ingen profil ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="c34a1-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34a1-118">-DefaultProfile</span></span>
<span data-ttu-id="c34a1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c34a1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-120">-DisableSetting</span></span>
<span data-ttu-id="c34a1-121">Inaktiverar en befintlig autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="c34a1-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="c34a1-122">-Location</span></span>
<span data-ttu-id="c34a1-123">Anger platsen för den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="c34a1-123">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c34a1-124">-Name</span></span>
<span data-ttu-id="c34a1-125">Anger namnet på den autoskalningsinställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c34a1-125">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-126">-Meddelande</span><span class="sxs-lookup"><span data-stu-id="c34a1-126">-Notification</span></span>
<span data-ttu-id="c34a1-127">Anger en lista med kommaavgränsade meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c34a1-127">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="c34a1-129">Anger namnet på resurs gruppen för resursen som är associerad med den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="c34a1-129">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-130">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="c34a1-130">-SettingSpec</span></span>
<span data-ttu-id="c34a1-131">Anger ett **AutoscaleSetting** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c34a1-131">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="c34a1-132">Du kan använda Get-AzureRmAutoscaleSetting cmdlet för att få ett **AutoscaleSetting** -objekt eller skapa ett i ett Windows PowerShell-skript.</span><span class="sxs-lookup"><span data-stu-id="c34a1-132">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c34a1-133">-TargetResourceId</span></span>
<span data-ttu-id="c34a1-134">Anger ID för resursen till Autoskala.</span><span class="sxs-lookup"><span data-stu-id="c34a1-134">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c34a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34a1-135">CommonParameters</span></span>
<span data-ttu-id="c34a1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c34a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34a1-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34a1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34a1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c34a1-138">INPUTS</span></span>

### <span data-ttu-id="c34a1-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="c34a1-139">None</span></span>
<span data-ttu-id="c34a1-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c34a1-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c34a1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c34a1-141">OUTPUTS</span></span>

### <span data-ttu-id="c34a1-142">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c34a1-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="c34a1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c34a1-143">NOTES</span></span>

## <span data-ttu-id="c34a1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c34a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="c34a1-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c34a1-146">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c34a1-146">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="c34a1-147">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c34a1-147">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="c34a1-148">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c34a1-148">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


