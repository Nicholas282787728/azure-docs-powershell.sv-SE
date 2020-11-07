---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 79ad0434a7918bbdf834b5917ed023cbbabf0525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755750"
---
# <span data-ttu-id="8d0d8-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d0d8-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="8d0d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0d8-103">Ändrar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d0d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d0d8-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d0d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d0d8-105">DESCRIPTION</span></span>
<span data-ttu-id="8d0d8-106">Cmdleten **set-AzureRmIntegrationAccountAgreement** ändrar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="8d0d8-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="8d0d8-108">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="8d0d8-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="8d0d8-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d0d8-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d0d8-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d0d8-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d0d8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d0d8-114">EXAMPLES</span></span>

### <span data-ttu-id="8d0d8-115">Exempel 1: uppdatera ett integrerings konto avtal</span><span class="sxs-lookup"><span data-stu-id="8d0d8-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN
                         . . .
```

<span data-ttu-id="8d0d8-116">Det här kommandot uppdaterar ett integrerings konto avtal i den angivna Azure resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="8d0d8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d0d8-117">PARAMETERS</span></span>

### <span data-ttu-id="8d0d8-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="8d0d8-118">-AgreementContent</span></span>
<span data-ttu-id="8d0d8-119">Anger avtalets innehåll i JSON-format (Java Object Notation) för avtalet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="8d0d8-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="8d0d8-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="8d0d8-121">Anger fil Sök vägen för avtalets innehåll.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="8d0d8-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8d0d8-122">-AgreementName</span></span>
<span data-ttu-id="8d0d8-123">Anger namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="8d0d8-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="8d0d8-124">-AgreementType</span></span>
<span data-ttu-id="8d0d8-125">Anger avtals typen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="8d0d8-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8d0d8-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d0d8-127">X12</span><span class="sxs-lookup"><span data-stu-id="8d0d8-127">X12</span></span> 
- <span data-ttu-id="8d0d8-128">AS2</span><span class="sxs-lookup"><span data-stu-id="8d0d8-128">AS2</span></span>
- <span data-ttu-id="8d0d8-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="8d0d8-129">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0d8-130">-DefaultProfile</span></span>
<span data-ttu-id="8d0d8-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d0d8-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d0d8-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8d0d8-132">-Force</span></span>
<span data-ttu-id="8d0d8-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="8d0d8-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="8d0d8-135">Anger en namn avgränsare för företags identitet för gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="8d0d8-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="8d0d8-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="8d0d8-137">Integrations konto avtalets värde för gäst identitet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="8d0d8-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="8d0d8-138">-GuestPartner</span></span>
<span data-ttu-id="8d0d8-139">Anger namnet på gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="8d0d8-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="8d0d8-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="8d0d8-141">Anger en namn avgränsare för företags identitet för värd partnern.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="8d0d8-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="8d0d8-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="8d0d8-143">Integrerings värde för värden för värd identitet för integrations konto avtal.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="8d0d8-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="8d0d8-144">-HostPartner</span></span>
<span data-ttu-id="8d0d8-145">Anger namnet på värd partnern.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="8d0d8-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8d0d8-146">-Metadata</span></span>
<span data-ttu-id="8d0d8-147">Anger ett metadataobjekt för avtalet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d0d8-148">-Name</span></span>
<span data-ttu-id="8d0d8-149">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-149">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d0d8-150">-ResourceGroupName</span></span>
<span data-ttu-id="8d0d8-151">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d0d8-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d0d8-152">-Confirm</span></span>
<span data-ttu-id="8d0d8-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0d8-154">-WhatIf</span></span>
<span data-ttu-id="8d0d8-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d0d8-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0d8-157">CommonParameters</span></span>
<span data-ttu-id="8d0d8-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0d8-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d0d8-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0d8-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d0d8-160">INPUTS</span></span>

### <span data-ttu-id="8d0d8-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="8d0d8-161">None</span></span>
<span data-ttu-id="8d0d8-162">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d0d8-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d0d8-163">OUTPUTS</span></span>

### <span data-ttu-id="8d0d8-164">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d0d8-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="8d0d8-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d0d8-165">NOTES</span></span>

## <span data-ttu-id="8d0d8-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d0d8-166">RELATED LINKS</span></span>

[<span data-ttu-id="8d0d8-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d0d8-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="8d0d8-168">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d0d8-168">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="8d0d8-169">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d0d8-169">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


