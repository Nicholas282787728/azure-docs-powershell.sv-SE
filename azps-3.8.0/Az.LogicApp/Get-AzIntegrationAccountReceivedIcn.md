---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926554"
---
# <span data-ttu-id="6eaf1-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6eaf1-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="6eaf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6eaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="6eaf1-103">Denna cmdlet hämtar ett specifikt mottaget utbytes kontroll nummer per avtal och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="6eaf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6eaf1-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eaf1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6eaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="6eaf1-106">Denna cmdlet är avsedd att användas vid katastrof återställning för att verifiera närvaron av ett mottaget utbytes kontroll nummer och, om du vill ta bort enheten med Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="6eaf1-107">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="6eaf1-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="6eaf1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6eaf1-108">EXAMPLES</span></span>

### <span data-ttu-id="6eaf1-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6eaf1-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="6eaf1-110">Med det här kommandot får du X12 integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="6eaf1-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6eaf1-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="6eaf1-112">Med det här kommandot får du EDIFACT integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="6eaf1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6eaf1-113">PARAMETERS</span></span>

### <span data-ttu-id="6eaf1-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6eaf1-114">-AgreementName</span></span>
<span data-ttu-id="6eaf1-115">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="6eaf1-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6eaf1-116">-AgreementType</span></span>
<span data-ttu-id="6eaf1-117">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="6eaf1-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="6eaf1-118">-ControlNumberValue</span></span>
<span data-ttu-id="6eaf1-119">Värdet på integrations kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="6eaf1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eaf1-120">-DefaultProfile</span></span>
<span data-ttu-id="6eaf1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6eaf1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eaf1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6eaf1-122">-Name</span></span>
<span data-ttu-id="6eaf1-123">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-123">The integration account name.</span></span>

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

### <span data-ttu-id="6eaf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eaf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="6eaf1-125">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="6eaf1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eaf1-126">CommonParameters</span></span>
<span data-ttu-id="6eaf1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eaf1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eaf1-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eaf1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eaf1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6eaf1-129">INPUTS</span></span>

### <span data-ttu-id="6eaf1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6eaf1-130">System.String</span></span>

## <span data-ttu-id="6eaf1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6eaf1-131">OUTPUTS</span></span>

### <span data-ttu-id="6eaf1-132">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="6eaf1-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="6eaf1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6eaf1-133">NOTES</span></span>

## <span data-ttu-id="6eaf1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6eaf1-134">RELATED LINKS</span></span>

[<span data-ttu-id="6eaf1-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6eaf1-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="6eaf1-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6eaf1-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
