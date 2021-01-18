---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525941"
---
# <span data-ttu-id="428aa-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="428aa-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="428aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="428aa-102">SYNOPSIS</span></span>
<span data-ttu-id="428aa-103">Hämtar integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="428aa-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="428aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="428aa-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="428aa-105">DESCRIPTION</span></span>
<span data-ttu-id="428aa-106">Cmdleten **Get-AzIntegrationAccountCertificate** hämtar integrerade konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="428aa-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="428aa-107">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="428aa-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="428aa-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="428aa-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="428aa-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="428aa-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="428aa-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="428aa-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="428aa-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="428aa-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="428aa-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="428aa-112">EXAMPLES</span></span>

### <span data-ttu-id="428aa-113">Exempel 1: skaffa ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="428aa-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="428aa-114">Det här kommandot får integrerings konto certifikatet med namnet IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="428aa-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="428aa-115">Exempel 2: skaffa certifikat för integrerings konton utifrån integrerings konto namn</span><span class="sxs-lookup"><span data-stu-id="428aa-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="428aa-116">Det här kommandot får integrerings konto certifikaten för integrations kontot med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="428aa-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="428aa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="428aa-117">PARAMETERS</span></span>

### <span data-ttu-id="428aa-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="428aa-118">-CertificateName</span></span>
<span data-ttu-id="428aa-119">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="428aa-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="428aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428aa-120">-DefaultProfile</span></span>
<span data-ttu-id="428aa-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="428aa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="428aa-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="428aa-122">-Name</span></span>
<span data-ttu-id="428aa-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="428aa-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="428aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="428aa-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="428aa-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="428aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428aa-126">CommonParameters</span></span>
<span data-ttu-id="428aa-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428aa-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428aa-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428aa-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="428aa-129">INPUTS</span></span>

### <span data-ttu-id="428aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="428aa-130">System.String</span></span>

## <span data-ttu-id="428aa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="428aa-131">OUTPUTS</span></span>

### <span data-ttu-id="428aa-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="428aa-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="428aa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="428aa-133">NOTES</span></span>

## <span data-ttu-id="428aa-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="428aa-134">RELATED LINKS</span></span>

[<span data-ttu-id="428aa-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="428aa-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="428aa-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="428aa-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="428aa-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="428aa-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


