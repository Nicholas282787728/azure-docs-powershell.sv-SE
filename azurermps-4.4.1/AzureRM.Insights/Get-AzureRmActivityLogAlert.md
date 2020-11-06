---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585523"
---
# <span data-ttu-id="134c0-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="134c0-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="134c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="134c0-102">SYNOPSIS</span></span>
<span data-ttu-id="134c0-103">Hämtar en eller flera aktivitets logg varningar.</span><span class="sxs-lookup"><span data-stu-id="134c0-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="134c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="134c0-104">SYNTAX</span></span>

### <span data-ttu-id="134c0-105">Standard parametrar för att få en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="134c0-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="134c0-106">Parametrar för att kontrol lera att resurs gruppen ges när namnet anges</span><span class="sxs-lookup"><span data-stu-id="134c0-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="134c0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="134c0-107">DESCRIPTION</span></span>
<span data-ttu-id="134c0-108">Cmdleten **Get-AzureRmActivityLogAlert** hämtar en eller flera aviserings resurser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="134c0-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="134c0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="134c0-109">EXAMPLES</span></span>

### <span data-ttu-id="134c0-110">Exempel 1: få en aktivitets loggs aviseringar efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="134c0-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="134c0-111">Det här kommandot listar alla aktivitets loggs aviseringar för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="134c0-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="134c0-112">Exempel 2: Hämta aktivitets logg meddelanden för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="134c0-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="134c0-113">Det här kommandot listar aktivitets loggnings aviseringar för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="134c0-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="134c0-114">Exempel 3: Hämta en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="134c0-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="134c0-115">Det här kommandot listar en (en lista med ett enskilt element) aktivitets logg varning.</span><span class="sxs-lookup"><span data-stu-id="134c0-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="134c0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="134c0-116">PARAMETERS</span></span>

### <span data-ttu-id="134c0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="134c0-117">-Name</span></span>
<span data-ttu-id="134c0-118">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="134c0-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="134c0-120">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="134c0-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="134c0-121">Om Name inte är null eller tomt måste den här parametern innehålla en sträng som inte är tom.</span><span class="sxs-lookup"><span data-stu-id="134c0-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134c0-122">-DefaultProfile</span></span>
<span data-ttu-id="134c0-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="134c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="134c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134c0-124">CommonParameters</span></span>
<span data-ttu-id="134c0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134c0-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="134c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134c0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="134c0-127">INPUTS</span></span>

### <span data-ttu-id="134c0-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="134c0-128">None</span></span>

## <span data-ttu-id="134c0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="134c0-129">OUTPUTS</span></span>

### <span data-ttu-id="134c0-130"><system. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="134c0-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="134c0-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="134c0-131">None</span></span>

## <span data-ttu-id="134c0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="134c0-132">NOTES</span></span>

## <span data-ttu-id="134c0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="134c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="134c0-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="134c0-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="134c0-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="134c0-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="134c0-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="134c0-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="134c0-137">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="134c0-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="134c0-138">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="134c0-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
