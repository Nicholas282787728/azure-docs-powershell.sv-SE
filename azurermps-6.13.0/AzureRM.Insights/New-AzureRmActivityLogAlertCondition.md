---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576985"
---
# <span data-ttu-id="47fd0-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="47fd0-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="47fd0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="47fd0-103">Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="47fd0-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47fd0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47fd0-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47fd0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="47fd0-106">**New-AzureRmActivityLogAlertCondition** cmdlet skapar ett nytt varnings objekt för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="47fd0-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="47fd0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="47fd0-108">Exempel 1: skapa ett nytt meddelande villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="47fd0-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="47fd0-109">Det här kommandot skapar ett nytt aviserings villkor för aktivitets loggning i minnet.</span><span class="sxs-lookup"><span data-stu-id="47fd0-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="47fd0-110">**Obs!** när den här cmdleten används med Set-AzureRmActivityLogAlert åtminstone ett av dessa objekt, som skickas som parametrar, måste dess fält vara lika med "Category".</span><span class="sxs-lookup"><span data-stu-id="47fd0-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="47fd0-111">Annars svarar Server gruppen med en 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="47fd0-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="47fd0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47fd0-112">PARAMETERS</span></span>

### <span data-ttu-id="47fd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fd0-113">-DefaultProfile</span></span>
<span data-ttu-id="47fd0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="47fd0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47fd0-115">-Lika med</span><span class="sxs-lookup"><span data-stu-id="47fd0-115">-Equal</span></span>
<span data-ttu-id="47fd0-116">Anger egenskapen Equals för löv villkoret.</span><span class="sxs-lookup"><span data-stu-id="47fd0-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="47fd0-117">-Fält</span><span class="sxs-lookup"><span data-stu-id="47fd0-117">-Field</span></span>
<span data-ttu-id="47fd0-118">Anger fältet för villkoret.</span><span class="sxs-lookup"><span data-stu-id="47fd0-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="47fd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fd0-119">CommonParameters</span></span>
<span data-ttu-id="47fd0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47fd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fd0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47fd0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fd0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47fd0-122">INPUTS</span></span>

### <span data-ttu-id="47fd0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="47fd0-123">System.String</span></span>

## <span data-ttu-id="47fd0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47fd0-124">OUTPUTS</span></span>

### <span data-ttu-id="47fd0-125">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="47fd0-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="47fd0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47fd0-126">NOTES</span></span>

## <span data-ttu-id="47fd0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47fd0-127">RELATED LINKS</span></span>

[<span data-ttu-id="47fd0-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47fd0-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47fd0-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47fd0-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47fd0-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47fd0-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47fd0-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47fd0-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47fd0-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="47fd0-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="47fd0-133">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="47fd0-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
