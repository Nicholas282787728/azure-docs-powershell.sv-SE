---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: eadd3052bb965b60bdaf377cd45fc014f25cac79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756503"
---
# <span data-ttu-id="1e269-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="1e269-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="1e269-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e269-102">SYNOPSIS</span></span>
<span data-ttu-id="1e269-103">Får ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="1e269-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e269-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e269-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e269-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e269-105">DESCRIPTION</span></span>
<span data-ttu-id="1e269-106">Cmdleten **Get-AzureRmIntegrationAccountAgreement** får ett integrerings konto avtal från en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="1e269-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="1e269-107">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="1e269-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="1e269-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="1e269-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1e269-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="1e269-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1e269-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="1e269-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1e269-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="1e269-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1e269-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e269-112">EXAMPLES</span></span>

### <span data-ttu-id="1e269-113">Exempel 1: skaffa ett integrerings konto avtal</span><span class="sxs-lookup"><span data-stu-id="1e269-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="1e269-114">Det här kommandot får ett integrerings konto avtal med namnet IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="1e269-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="1e269-115">Exempel 2: skaffa integrerings konto avtal efter resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="1e269-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="1e269-116">Det här kommandot får integrerings konto avtal per resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="1e269-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="1e269-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e269-117">PARAMETERS</span></span>

### <span data-ttu-id="1e269-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1e269-118">-AgreementName</span></span>
<span data-ttu-id="1e269-119">Anger namnet på ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="1e269-119">Specifies the name of an integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e269-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e269-120">-DefaultProfile</span></span>
<span data-ttu-id="1e269-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1e269-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e269-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e269-122">-Name</span></span>
<span data-ttu-id="1e269-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="1e269-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e269-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e269-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e269-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1e269-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e269-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e269-126">CommonParameters</span></span>
<span data-ttu-id="1e269-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e269-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e269-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e269-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e269-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e269-129">INPUTS</span></span>

### <span data-ttu-id="1e269-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="1e269-130">None</span></span>
<span data-ttu-id="1e269-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1e269-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e269-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e269-132">OUTPUTS</span></span>

### <span data-ttu-id="1e269-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="1e269-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="1e269-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e269-134">NOTES</span></span>

## <span data-ttu-id="1e269-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e269-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e269-136">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="1e269-136">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="1e269-137">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="1e269-137">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="1e269-138">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="1e269-138">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


