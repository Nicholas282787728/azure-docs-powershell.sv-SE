---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926593"
---
# <span data-ttu-id="9dd00-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9dd00-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="9dd00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dd00-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd00-103">Får ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="9dd00-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="9dd00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dd00-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd00-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dd00-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd00-106">Cmdleten **Get-AzIntegrationAccountAgreement** får ett integrerings konto avtal från en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="9dd00-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="9dd00-107">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="9dd00-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="9dd00-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="9dd00-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9dd00-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="9dd00-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9dd00-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9dd00-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9dd00-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="9dd00-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9dd00-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dd00-112">EXAMPLES</span></span>

### <span data-ttu-id="9dd00-113">Exempel 1: skaffa ett integrerings konto avtal</span><span class="sxs-lookup"><span data-stu-id="9dd00-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="9dd00-114">Det här kommandot får ett integrerings konto avtal med namnet IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="9dd00-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="9dd00-115">Exempel 2: skaffa integrerings konto avtal efter resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="9dd00-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="9dd00-116">Det här kommandot får integrerings konto avtal per resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="9dd00-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="9dd00-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dd00-117">PARAMETERS</span></span>

### <span data-ttu-id="9dd00-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="9dd00-118">-AgreementName</span></span>
<span data-ttu-id="9dd00-119">Anger namnet på ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="9dd00-119">Specifies the name of an integration account agreement.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd00-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd00-120">-DefaultProfile</span></span>
<span data-ttu-id="9dd00-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9dd00-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd00-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9dd00-122">-Name</span></span>
<span data-ttu-id="9dd00-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="9dd00-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd00-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dd00-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9dd00-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd00-126">CommonParameters</span></span>
<span data-ttu-id="9dd00-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd00-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd00-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd00-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dd00-129">INPUTS</span></span>

### <span data-ttu-id="9dd00-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9dd00-130">System.String</span></span>

## <span data-ttu-id="9dd00-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dd00-131">OUTPUTS</span></span>

### <span data-ttu-id="9dd00-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9dd00-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="9dd00-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dd00-133">NOTES</span></span>

## <span data-ttu-id="9dd00-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dd00-134">RELATED LINKS</span></span>

[<span data-ttu-id="9dd00-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9dd00-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="9dd00-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9dd00-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="9dd00-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="9dd00-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


