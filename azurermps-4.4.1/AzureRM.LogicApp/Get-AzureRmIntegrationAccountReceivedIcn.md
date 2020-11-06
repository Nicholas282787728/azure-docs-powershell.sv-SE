---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574625"
---
# <span data-ttu-id="ae8f8-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ae8f8-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="ae8f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8f8-103">Denna cmdlet hämtar ett specifikt mottaget utbytes kontroll nummer per avtal och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae8f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae8f8-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae8f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8f8-106">Denna cmdlet är avsedd att användas vid katastrof återställning för att verifiera närvaron av ett mottaget utbytes kontroll nummer och, om du vill ta bort enheten med Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="ae8f8-107">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="ae8f8-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ae8f8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae8f8-108">EXAMPLES</span></span>

### <span data-ttu-id="ae8f8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae8f8-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="ae8f8-110">Med det här kommandot får du X12 integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="ae8f8-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ae8f8-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="ae8f8-112">Med det här kommandot får du EDIFACT integrerings konto för utbytes kontroll nummer efter avtals namn och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="ae8f8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae8f8-113">PARAMETERS</span></span>

### <span data-ttu-id="ae8f8-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="ae8f8-114">-AgreementName</span></span>
<span data-ttu-id="ae8f8-115">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="ae8f8-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="ae8f8-116">-ControlNumberValue</span></span>
<span data-ttu-id="ae8f8-117">Värdet på integrations kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="ae8f8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae8f8-118">-Name</span></span>
<span data-ttu-id="ae8f8-119">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-119">The integration account name.</span></span>

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

### <span data-ttu-id="ae8f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae8f8-121">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ae8f8-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="ae8f8-122">-AgreementType</span></span>
<span data-ttu-id="ae8f8-123">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8f8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8f8-124">-DefaultProfile</span></span>
<span data-ttu-id="ae8f8-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae8f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8f8-126">CommonParameters</span></span>
<span data-ttu-id="ae8f8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae8f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8f8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae8f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8f8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae8f8-129">INPUTS</span></span>

### <span data-ttu-id="ae8f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ae8f8-130">System.String</span></span>

## <span data-ttu-id="ae8f8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae8f8-131">OUTPUTS</span></span>

### <span data-ttu-id="ae8f8-132">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="ae8f8-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ae8f8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae8f8-133">NOTES</span></span>

## <span data-ttu-id="ae8f8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae8f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae8f8-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ae8f8-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="ae8f8-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ae8f8-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
