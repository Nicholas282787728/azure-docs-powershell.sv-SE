---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271839"
---
# <span data-ttu-id="02ae5-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="02ae5-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="02ae5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="02ae5-103">Hämtar en eller flera aktivitets logg varningar.</span><span class="sxs-lookup"><span data-stu-id="02ae5-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="02ae5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02ae5-104">SYNTAX</span></span>

### <span data-ttu-id="02ae5-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02ae5-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ae5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02ae5-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02ae5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="02ae5-108">Cmdleten **Get-AzActivityLogAlert** hämtar en eller flera aviserings resurser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="02ae5-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="02ae5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="02ae5-110">Exempel 1: få en aktivitets loggs aviseringar efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="02ae5-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="02ae5-111">Det här kommandot listar alla aktivitets loggs aviseringar för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="02ae5-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="02ae5-112">Exempel 2: Hämta aktivitets logg meddelanden för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="02ae5-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="02ae5-113">Det här kommandot listar aktivitets loggnings aviseringar för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02ae5-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="02ae5-114">Exempel 3: Hämta en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="02ae5-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="02ae5-115">Det här kommandot listar en (en lista med ett enskilt element) aktivitets logg varning.</span><span class="sxs-lookup"><span data-stu-id="02ae5-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="02ae5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02ae5-116">PARAMETERS</span></span>

### <span data-ttu-id="02ae5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ae5-117">-DefaultProfile</span></span>
<span data-ttu-id="02ae5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02ae5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02ae5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="02ae5-119">-Name</span></span>
<span data-ttu-id="02ae5-120">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="02ae5-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="02ae5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ae5-121">-ResourceGroupName</span></span>
<span data-ttu-id="02ae5-122">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="02ae5-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="02ae5-123">Om Name inte är null eller tomt måste den här parametern innehålla en sträng som inte är tom.</span><span class="sxs-lookup"><span data-stu-id="02ae5-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="02ae5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ae5-124">CommonParameters</span></span>
<span data-ttu-id="02ae5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ae5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ae5-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ae5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ae5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02ae5-127">INPUTS</span></span>

### <span data-ttu-id="02ae5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="02ae5-128">System.String</span></span>

## <span data-ttu-id="02ae5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02ae5-129">OUTPUTS</span></span>

### <span data-ttu-id="02ae5-130">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="02ae5-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="02ae5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02ae5-131">NOTES</span></span>

## <span data-ttu-id="02ae5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02ae5-132">RELATED LINKS</span></span>

[<span data-ttu-id="02ae5-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="02ae5-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="02ae5-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="02ae5-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="02ae5-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="02ae5-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="02ae5-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="02ae5-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="02ae5-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="02ae5-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)