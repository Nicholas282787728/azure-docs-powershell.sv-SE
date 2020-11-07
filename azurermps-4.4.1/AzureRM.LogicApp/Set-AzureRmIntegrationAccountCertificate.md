---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: feb885ca6f08a7396fd88db73d48172dc002f055
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582367"
---
# <span data-ttu-id="9b67f-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9b67f-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="9b67f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b67f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b67f-103">Ändrar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="9b67f-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b67f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b67f-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b67f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b67f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b67f-106">Cmdleten **set-AzureRmIntegrationAccountCertificate** ändrar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="9b67f-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="9b67f-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b67f-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="9b67f-108">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="9b67f-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="9b67f-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="9b67f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9b67f-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="9b67f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9b67f-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9b67f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9b67f-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="9b67f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9b67f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b67f-113">EXAMPLES</span></span>

### <span data-ttu-id="9b67f-114">Exempel 1: ändra ett integrations konto certifikat</span><span class="sxs-lookup"><span data-stu-id="9b67f-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="9b67f-115">Det här kommandot ändrar det integrerade konto certifikatet i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b67f-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="9b67f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b67f-116">PARAMETERS</span></span>

### <span data-ttu-id="9b67f-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9b67f-117">-CertificateName</span></span>
<span data-ttu-id="9b67f-118">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="9b67f-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="9b67f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9b67f-119">-Force</span></span>
<span data-ttu-id="9b67f-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9b67f-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b67f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b67f-121">-KeyName</span></span>
<span data-ttu-id="9b67f-122">Anger namnet på en certifikats nycklar i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="9b67f-122">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="9b67f-123">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9b67f-123">-KeyVaultId</span></span>
<span data-ttu-id="9b67f-124">Anger ett valv-ID.</span><span class="sxs-lookup"><span data-stu-id="9b67f-124">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="9b67f-125">-Version</span><span class="sxs-lookup"><span data-stu-id="9b67f-125">-KeyVersion</span></span>
<span data-ttu-id="9b67f-126">Anger vilken version av certifikats nycklar som visas i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="9b67f-126">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="9b67f-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9b67f-127">-Metadata</span></span>
<span data-ttu-id="9b67f-128">Anger ett metadataobjekt för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b67f-128">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b67f-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b67f-129">-Name</span></span>
<span data-ttu-id="9b67f-130">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="9b67f-130">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b67f-131">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="9b67f-131">-PublicCertificateFilePath</span></span>
<span data-ttu-id="9b67f-132">Anger sökvägen till ett offentlig certifikat (CER-fil).</span><span class="sxs-lookup"><span data-stu-id="9b67f-132">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="9b67f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b67f-133">-ResourceGroupName</span></span>
<span data-ttu-id="9b67f-134">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9b67f-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b67f-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b67f-135">-Confirm</span></span>
<span data-ttu-id="9b67f-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b67f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b67f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b67f-137">-WhatIf</span></span>
<span data-ttu-id="9b67f-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b67f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b67f-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b67f-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b67f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b67f-140">-DefaultProfile</span></span>
<span data-ttu-id="9b67f-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b67f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b67f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b67f-142">CommonParameters</span></span>
<span data-ttu-id="9b67f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b67f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b67f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b67f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b67f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b67f-145">INPUTS</span></span>

## <span data-ttu-id="9b67f-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b67f-146">OUTPUTS</span></span>

### <span data-ttu-id="9b67f-147">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9b67f-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="9b67f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b67f-148">NOTES</span></span>

## <span data-ttu-id="9b67f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b67f-149">RELATED LINKS</span></span>

[<span data-ttu-id="9b67f-150">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9b67f-150">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9b67f-151">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9b67f-151">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9b67f-152">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9b67f-152">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

