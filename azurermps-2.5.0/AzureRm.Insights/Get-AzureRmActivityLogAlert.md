---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: af8ef3ef2662dc6793011741fdfd7a903eaa081f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931421"
---
# <span data-ttu-id="99109-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="99109-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="99109-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99109-102">SYNOPSIS</span></span>
<span data-ttu-id="99109-103">Hämtar en eller flera aktivitets logg varningar.</span><span class="sxs-lookup"><span data-stu-id="99109-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99109-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99109-104">SYNTAX</span></span>

### <span data-ttu-id="99109-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99109-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99109-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99109-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99109-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99109-107">DESCRIPTION</span></span>
<span data-ttu-id="99109-108">Cmdleten **Get-AzureRmActivityLogAlert** hämtar en eller flera aviserings resurser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="99109-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="99109-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99109-109">EXAMPLES</span></span>

### <span data-ttu-id="99109-110">Exempel 1: få en aktivitets loggs aviseringar efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="99109-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="99109-111">Det här kommandot listar alla aktivitets loggs aviseringar för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="99109-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="99109-112">Exempel 2: Hämta aktivitets logg meddelanden för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="99109-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="99109-113">Det här kommandot listar aktivitets loggnings aviseringar för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="99109-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="99109-114">Exempel 3: Hämta en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="99109-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="99109-115">Det här kommandot listar en (en lista med ett enskilt element) aktivitets logg varning.</span><span class="sxs-lookup"><span data-stu-id="99109-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="99109-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99109-116">PARAMETERS</span></span>

### <span data-ttu-id="99109-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99109-117">-DefaultProfile</span></span>
<span data-ttu-id="99109-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99109-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99109-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="99109-119">-Name</span></span>
<span data-ttu-id="99109-120">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="99109-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99109-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99109-121">-ResourceGroupName</span></span>
<span data-ttu-id="99109-122">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="99109-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="99109-123">Om Name inte är null eller tomt måste den här parametern innehålla en sträng som inte är tom.</span><span class="sxs-lookup"><span data-stu-id="99109-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99109-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99109-124">CommonParameters</span></span>
<span data-ttu-id="99109-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99109-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99109-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99109-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99109-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99109-127">INPUTS</span></span>

### <span data-ttu-id="99109-128">System. String</span><span class="sxs-lookup"><span data-stu-id="99109-128">System.String</span></span>

## <span data-ttu-id="99109-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99109-129">OUTPUTS</span></span>

### <span data-ttu-id="99109-130">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="99109-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="99109-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99109-131">NOTES</span></span>

## <span data-ttu-id="99109-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99109-132">RELATED LINKS</span></span>

[<span data-ttu-id="99109-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="99109-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)



[<span data-ttu-id="99109-134">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="99109-134">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="99109-135">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="99109-135">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="99109-136">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="99109-136">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
