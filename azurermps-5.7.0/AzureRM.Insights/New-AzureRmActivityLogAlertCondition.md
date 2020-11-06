---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: d9309f2de88dc87368b510cdf6f1062d03c7f709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577215"
---
# <span data-ttu-id="53bd1-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="53bd1-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="53bd1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="53bd1-103">Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="53bd1-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bd1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53bd1-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53bd1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="53bd1-106">**New-AzureRmActivityLogAlertCondition** cmdlet skapar ett nytt varnings objekt för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="53bd1-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="53bd1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53bd1-107">EXAMPLES</span></span>

### <span data-ttu-id="53bd1-108">Exempel 1: skapa ett nytt meddelande villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="53bd1-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="53bd1-109">Det här kommandot skapar ett nytt aviserings villkor för aktivitets loggning i minnet.</span><span class="sxs-lookup"><span data-stu-id="53bd1-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="53bd1-110">**Obs!** när den här cmdleten används med Set-AzureRmActivityLogAlert åtminstone ett av dessa objekt, som skickas som parametrar, måste dess fält vara lika med "Category".</span><span class="sxs-lookup"><span data-stu-id="53bd1-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="53bd1-111">Annars svarar Server gruppen med en 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="53bd1-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="53bd1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53bd1-112">PARAMETERS</span></span>

### <span data-ttu-id="53bd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bd1-113">-DefaultProfile</span></span>
<span data-ttu-id="53bd1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="53bd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53bd1-115">-Lika med</span><span class="sxs-lookup"><span data-stu-id="53bd1-115">-Equal</span></span>
<span data-ttu-id="53bd1-116">Anger egenskapen Equals för löv villkoret.</span><span class="sxs-lookup"><span data-stu-id="53bd1-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bd1-117">-Fält</span><span class="sxs-lookup"><span data-stu-id="53bd1-117">-Field</span></span>
<span data-ttu-id="53bd1-118">Anger fältet för villkoret.</span><span class="sxs-lookup"><span data-stu-id="53bd1-118">Specifies the field for the condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bd1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bd1-119">CommonParameters</span></span>
<span data-ttu-id="53bd1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bd1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bd1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bd1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bd1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53bd1-122">INPUTS</span></span>

### <span data-ttu-id="53bd1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="53bd1-123">None</span></span>
<span data-ttu-id="53bd1-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="53bd1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53bd1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53bd1-125">OUTPUTS</span></span>

### <span data-ttu-id="53bd1-126">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="53bd1-126">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="53bd1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53bd1-127">NOTES</span></span>

## <span data-ttu-id="53bd1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53bd1-128">RELATED LINKS</span></span>

[<span data-ttu-id="53bd1-129">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="53bd1-129">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="53bd1-130">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="53bd1-130">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="53bd1-131">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="53bd1-131">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="53bd1-132">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="53bd1-132">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="53bd1-133">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="53bd1-133">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="53bd1-134">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="53bd1-134">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
