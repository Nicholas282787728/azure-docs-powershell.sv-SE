---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: b9defadc92619d136c82302203d296d6b71318ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576250"
---
# <span data-ttu-id="9a136-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9a136-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="9a136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a136-102">SYNOPSIS</span></span>
<span data-ttu-id="9a136-103">Denna cmdlet hämtar ett specifikt mottaget utbytes kontroll nummer per avtal och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="9a136-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a136-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a136-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a136-105">DESCRIPTION</span></span>
<span data-ttu-id="9a136-106">Denna cmdlet är avsedd att användas vid katastrof återställning för att verifiera närvaron av ett mottaget utbytes kontroll nummer och, om du vill ta bort enheten med Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="9a136-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="9a136-107">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="9a136-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="9a136-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a136-108">EXAMPLES</span></span>

### <span data-ttu-id="9a136-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a136-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="9a136-110">Med det här kommandot får du X12 integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="9a136-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="9a136-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9a136-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="9a136-112">Med det här kommandot får du EDIFACT integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="9a136-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="9a136-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a136-113">PARAMETERS</span></span>

### <span data-ttu-id="9a136-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="9a136-114">-AgreementName</span></span>
<span data-ttu-id="9a136-115">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="9a136-115">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a136-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="9a136-116">-AgreementType</span></span>
<span data-ttu-id="9a136-117">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="9a136-117">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a136-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="9a136-118">-ControlNumberValue</span></span>
<span data-ttu-id="9a136-119">Värdet på integrations kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="9a136-119">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a136-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a136-120">-DefaultProfile</span></span>
<span data-ttu-id="9a136-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9a136-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a136-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a136-122">-Name</span></span>
<span data-ttu-id="9a136-123">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="9a136-123">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a136-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a136-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a136-125">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="9a136-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="9a136-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a136-126">CommonParameters</span></span>
<span data-ttu-id="9a136-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a136-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a136-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a136-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a136-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a136-129">INPUTS</span></span>

### <span data-ttu-id="9a136-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9a136-130">System.String</span></span>

## <span data-ttu-id="9a136-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a136-131">OUTPUTS</span></span>

### <span data-ttu-id="9a136-132">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="9a136-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="9a136-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a136-133">NOTES</span></span>

## <span data-ttu-id="9a136-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a136-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a136-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9a136-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="9a136-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9a136-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
