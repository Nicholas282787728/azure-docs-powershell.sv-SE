---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320987"
---
# <span data-ttu-id="9a7f5-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9a7f5-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="9a7f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7f5-103">Hämta status för prenumerationen för händelse utlösaren till angivna externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="9a7f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a7f5-104">SYNTAX</span></span>

### <span data-ttu-id="9a7f5-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9a7f5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a7f5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a7f5-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a7f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a7f5-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a7f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a7f5-108">DESCRIPTION</span></span>
<span data-ttu-id="9a7f5-109">Det här kommandot får statusen för abonnemanget för händelse utlösaren till angivna externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="9a7f5-110">Utlösaren kan inte startas förrän den returnerade statusen är "aktive rad".</span><span class="sxs-lookup"><span data-stu-id="9a7f5-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="9a7f5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a7f5-111">EXAMPLES</span></span>

### <span data-ttu-id="9a7f5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a7f5-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="9a7f5-113">Det här kommandot får statusen för subscribtion för BlobEnetTrigger1-utlösare för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="9a7f5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a7f5-114">PARAMETERS</span></span>

### <span data-ttu-id="9a7f5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9a7f5-115">-DataFactoryName</span></span>
<span data-ttu-id="9a7f5-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7f5-117">-DefaultProfile</span></span>
<span data-ttu-id="9a7f5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7f5-119">-InputObject</span></span>
<span data-ttu-id="9a7f5-120">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a7f5-121">-Name</span></span>
<span data-ttu-id="9a7f5-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a7f5-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a7f5-125">-ResourceId</span></span>
<span data-ttu-id="9a7f5-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a7f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7f5-127">CommonParameters</span></span>
<span data-ttu-id="9a7f5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7f5-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7f5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7f5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a7f5-130">INPUTS</span></span>

### <span data-ttu-id="9a7f5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9a7f5-131">System.String</span></span>
<span data-ttu-id="9a7f5-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9a7f5-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9a7f5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a7f5-133">OUTPUTS</span></span>

### <span data-ttu-id="9a7f5-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9a7f5-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="9a7f5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a7f5-135">NOTES</span></span>

## <span data-ttu-id="9a7f5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a7f5-136">RELATED LINKS</span></span>

