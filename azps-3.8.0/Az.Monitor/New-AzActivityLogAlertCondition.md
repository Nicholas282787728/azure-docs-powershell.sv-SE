---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090711"
---
# <span data-ttu-id="ac46b-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ac46b-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="ac46b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac46b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac46b-103">Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="ac46b-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ac46b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac46b-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac46b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac46b-105">DESCRIPTION</span></span>
<span data-ttu-id="ac46b-106">**New-AzActivityLogAlertCondition** cmdlet skapar ett nytt varnings objekt för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="ac46b-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ac46b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac46b-107">EXAMPLES</span></span>

### <span data-ttu-id="ac46b-108">Exempel 1: skapa ett nytt meddelande villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="ac46b-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="ac46b-109">Det här kommandot skapar ett nytt aviserings villkor för aktivitets loggning i minnet.</span><span class="sxs-lookup"><span data-stu-id="ac46b-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="ac46b-110">**Obs!** när den här cmdleten används med Set-AzActivityLogAlert åtminstone ett av dessa objekt, som skickas som parametrar, måste dess fält vara lika med "Category".</span><span class="sxs-lookup"><span data-stu-id="ac46b-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="ac46b-111">Annars svarar Server gruppen med en 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="ac46b-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="ac46b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac46b-112">PARAMETERS</span></span>

### <span data-ttu-id="ac46b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac46b-113">-DefaultProfile</span></span>
<span data-ttu-id="ac46b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ac46b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac46b-115">-Lika med</span><span class="sxs-lookup"><span data-stu-id="ac46b-115">-Equal</span></span>
<span data-ttu-id="ac46b-116">Anger egenskapen Equals för löv villkoret.</span><span class="sxs-lookup"><span data-stu-id="ac46b-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="ac46b-117">-Fält</span><span class="sxs-lookup"><span data-stu-id="ac46b-117">-Field</span></span>
<span data-ttu-id="ac46b-118">Anger fältet för villkoret.</span><span class="sxs-lookup"><span data-stu-id="ac46b-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="ac46b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac46b-119">CommonParameters</span></span>
<span data-ttu-id="ac46b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac46b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac46b-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac46b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac46b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac46b-122">INPUTS</span></span>

### <span data-ttu-id="ac46b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ac46b-123">System.String</span></span>

## <span data-ttu-id="ac46b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac46b-124">OUTPUTS</span></span>

### <span data-ttu-id="ac46b-125">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="ac46b-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="ac46b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac46b-126">NOTES</span></span>

## <span data-ttu-id="ac46b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac46b-127">RELATED LINKS</span></span>

[<span data-ttu-id="ac46b-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ac46b-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ac46b-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ac46b-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="ac46b-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ac46b-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="ac46b-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ac46b-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="ac46b-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ac46b-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="ac46b-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ac46b-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
