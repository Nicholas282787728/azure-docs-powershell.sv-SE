---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 3d26bca20befc31edfa437c7d3f9bc5dfced2b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574635"
---
# <span data-ttu-id="65227-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="65227-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="65227-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65227-102">SYNOPSIS</span></span>
<span data-ttu-id="65227-103">Hämtar integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="65227-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65227-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65227-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65227-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65227-105">DESCRIPTION</span></span>
<span data-ttu-id="65227-106">Cmdleten **Get-AzureRmIntegrationAccountCertificate** hämtar integrerade konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="65227-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="65227-107">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="65227-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="65227-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="65227-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="65227-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="65227-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="65227-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="65227-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="65227-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="65227-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="65227-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65227-112">EXAMPLES</span></span>

### <span data-ttu-id="65227-113">Exempel 1: skaffa ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="65227-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="65227-114">Det här kommandot får integrerings konto certifikatet med namnet IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="65227-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="65227-115">Exempel 2: skaffa certifikat för integrerings konton utifrån integrerings konto namn</span><span class="sxs-lookup"><span data-stu-id="65227-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="65227-116">Det här kommandot får integrerings konto certifikaten för integrations kontot med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="65227-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="65227-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65227-117">PARAMETERS</span></span>

### <span data-ttu-id="65227-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="65227-118">-CertificateName</span></span>
<span data-ttu-id="65227-119">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="65227-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="65227-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="65227-120">-Name</span></span>
<span data-ttu-id="65227-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="65227-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="65227-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65227-122">-ResourceGroupName</span></span>
<span data-ttu-id="65227-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="65227-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="65227-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65227-124">-DefaultProfile</span></span>
<span data-ttu-id="65227-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65227-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65227-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65227-126">CommonParameters</span></span>
<span data-ttu-id="65227-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65227-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65227-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65227-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65227-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65227-129">INPUTS</span></span>

## <span data-ttu-id="65227-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65227-130">OUTPUTS</span></span>

### <span data-ttu-id="65227-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="65227-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="65227-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65227-132">NOTES</span></span>

## <span data-ttu-id="65227-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65227-133">RELATED LINKS</span></span>

[<span data-ttu-id="65227-134">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="65227-134">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="65227-135">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="65227-135">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="65227-136">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="65227-136">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


