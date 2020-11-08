---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 23dd49b6c331f29111c6e203517d815ee6b24b53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918613"
---
# <span data-ttu-id="2e0b7-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2e0b7-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="2e0b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0b7-103">Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="2e0b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e0b7-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e0b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0b7-106">**New-AzActivityLogAlertCondition** cmdlet skapar ett nytt varnings objekt för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="2e0b7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e0b7-107">EXAMPLES</span></span>

### <span data-ttu-id="2e0b7-108">Exempel 1: skapa ett nytt meddelande villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="2e0b7-109">Det här kommandot skapar ett nytt aviserings villkor för aktivitets loggning i minnet.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="2e0b7-110">**Obs!** när den här cmdleten används med Set-AzActivityLogAlert åtminstone ett av dessa objekt, som skickas som parametrar, måste dess fält vara lika med "Category".</span><span class="sxs-lookup"><span data-stu-id="2e0b7-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="2e0b7-111">Annars svarar Server gruppen med en 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="2e0b7-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="2e0b7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e0b7-112">PARAMETERS</span></span>

### <span data-ttu-id="2e0b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0b7-113">-DefaultProfile</span></span>
<span data-ttu-id="2e0b7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2e0b7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e0b7-115">-Lika med</span><span class="sxs-lookup"><span data-stu-id="2e0b7-115">-Equal</span></span>
<span data-ttu-id="2e0b7-116">Anger egenskapen Equals för löv villkoret.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="2e0b7-117">-Fält</span><span class="sxs-lookup"><span data-stu-id="2e0b7-117">-Field</span></span>
<span data-ttu-id="2e0b7-118">Anger fältet för villkoret.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="2e0b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0b7-119">CommonParameters</span></span>
<span data-ttu-id="2e0b7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0b7-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e0b7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0b7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e0b7-122">INPUTS</span></span>

### <span data-ttu-id="2e0b7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0b7-123">System.String</span></span>

## <span data-ttu-id="2e0b7-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e0b7-124">OUTPUTS</span></span>

### <span data-ttu-id="2e0b7-125">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="2e0b7-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="2e0b7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e0b7-126">NOTES</span></span>

## <span data-ttu-id="2e0b7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e0b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="2e0b7-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e0b7-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2e0b7-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e0b7-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="2e0b7-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e0b7-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="2e0b7-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e0b7-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="2e0b7-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e0b7-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2e0b7-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2e0b7-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)