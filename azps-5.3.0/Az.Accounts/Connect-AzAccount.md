---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523368"
---
# <span data-ttu-id="c66a2-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c66a2-101">Connect-AzAccount</span></span>

## <span data-ttu-id="c66a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c66a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c66a2-103">Anslut till Azure med ett autentiserat konto som ska användas med cmdletar från AZ PowerShell-moduler.</span><span class="sxs-lookup"><span data-stu-id="c66a2-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="c66a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c66a2-104">SYNTAX</span></span>

### <span data-ttu-id="c66a2-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="c66a2-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c66a2-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c66a2-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c66a2-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="c66a2-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c66a2-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c66a2-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c66a2-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c66a2-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c66a2-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="c66a2-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c66a2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c66a2-111">DESCRIPTION</span></span>

<span data-ttu-id="c66a2-112">`Connect-AzAccount`Cmdleten ansluter till Azure med ett autentiserat konto som ska användas med cmdletar från AZ PowerShell-moduler.</span><span class="sxs-lookup"><span data-stu-id="c66a2-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="c66a2-113">Du kan endast använda detta autentiserade konto med Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="c66a2-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="c66a2-114">Om du vill lägga till ett autentiserat konto för användning med tjänst hantering använder du `Add-AzureAccount` cmdleten från Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="c66a2-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="c66a2-115">Om ingen kontext hittas för den aktuella användaren fylls användarens kontext lista i med en kontext för var och en av sina första 25 prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="c66a2-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="c66a2-116">Listan med kontexter som skapas för användaren kan hittas genom att köra `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="c66a2-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="c66a2-117">Om du vill hoppa över den här kontext populationen anger du **SkipContextPopulation** -växeln.</span><span class="sxs-lookup"><span data-stu-id="c66a2-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="c66a2-118">När du har kört denna cmdlet kan du koppla ner från ett Azure-konto med `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="c66a2-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="c66a2-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c66a2-119">EXAMPLES</span></span>

### <span data-ttu-id="c66a2-120">Exempel 1: Anslut till ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="c66a2-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="c66a2-121">Det här exemplet ansluter till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="c66a2-121">This example connects to an Azure account.</span></span> <span data-ttu-id="c66a2-122">Du måste ange autentiseringsuppgifter för ett Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="c66a2-123">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="c66a2-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-124">Exempel 2: (endast Windows PowerShell 5,1) Anslut till Azure med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="c66a2-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="c66a2-125">Det här scenariot fungerar bara i Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="c66a2-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="c66a2-126">Första kommandot frågar efter användarautentiseringsuppgifter och lagrar dem i `$Credential` variabeln.</span><span class="sxs-lookup"><span data-stu-id="c66a2-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c66a2-127">Det andra kommandot ansluter till ett Azure-konto med de inloggnings uppgifter som lagras i `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="c66a2-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="c66a2-128">Det här kontot autentiseras med Azure med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-129">Exempel 3: ansluta till Azure med ett SPN-konto</span><span class="sxs-lookup"><span data-stu-id="c66a2-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="c66a2-130">Den första kommando raden för tjänstens huvud referenser och lagrar dem i `$Credential` variabeln.</span><span class="sxs-lookup"><span data-stu-id="c66a2-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="c66a2-131">Ange ditt program-ID för användar namn och tjänste princip hemlighet som lösen ordet när du uppmanas att göra det.</span><span class="sxs-lookup"><span data-stu-id="c66a2-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="c66a2-132">Det andra kommandot ansluter den angivna Azure-klient organisationen med de tjänst huvud referenser som lagras i `$Credential` variabeln.</span><span class="sxs-lookup"><span data-stu-id="c66a2-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="c66a2-133">Parametern **ServicePrincipal** anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c66a2-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-134">Exempel 4: använda en interaktiv inloggning för att ansluta till en specifik klient organisation och ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c66a2-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="c66a2-135">Det här exemplet ansluter till ett Azure-konto med angiven klient organisation och prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c66a2-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-136">Exempel 5: Anslut med en hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="c66a2-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="c66a2-137">Det här exemplet ansluter med hjälp av värd miljöns MSI (Managed Service Identity).</span><span class="sxs-lookup"><span data-stu-id="c66a2-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="c66a2-138">Du loggar till exempel in till Azure från en virtuell dator som har en tilldelad MSI.</span><span class="sxs-lookup"><span data-stu-id="c66a2-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-139">Exempel 6: Anslut med hjälp av inloggnings-och ClientId för hanterad tjänst</span><span class="sxs-lookup"><span data-stu-id="c66a2-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="c66a2-140">Det här exemplet ansluter med den hanterade tjänstens identitet för **myUserAssignedIdentity**.</span><span class="sxs-lookup"><span data-stu-id="c66a2-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="c66a2-141">Den användare tilldelade identiteten läggs till på den virtuella datorn och ansluts sedan med ClientId för den användare som tilldelats identiteten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="c66a2-142">Mer information finns i [Konfigurera hanterade identiteter för Azure-resurser på en Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="c66a2-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="c66a2-143">Exempel 7: Anslut med certifikat</span><span class="sxs-lookup"><span data-stu-id="c66a2-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="c66a2-144">I det här exemplet ansluts du till ett Azure-konto med certifikatbaserad tjänstens huvud identifiering.</span><span class="sxs-lookup"><span data-stu-id="c66a2-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="c66a2-145">Tjänstens huvud namn som används för auktorisering måste skapas med det angivna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c66a2-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="c66a2-146">Mer information om hur du skapar ett självsignerat certifikat och tilldelar dem behörigheter finns i [använda Azure PowerShell för att skapa ett tjänst huvud med ett certifikat](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="c66a2-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="c66a2-147">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c66a2-147">PARAMETERS</span></span>

### <span data-ttu-id="c66a2-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="c66a2-148">-AccessToken</span></span>

<span data-ttu-id="c66a2-149">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="c66a2-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="c66a2-150">Åtkomsttoken är en typ av autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="c66a2-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="c66a2-151">Du bör vidta lämpliga säkerhets åtgärder för att skydda dem.</span><span class="sxs-lookup"><span data-stu-id="c66a2-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="c66a2-152">Även tids gränser för åtkomsttoken och kan förhindra att aktiviteter slutförs.</span><span class="sxs-lookup"><span data-stu-id="c66a2-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="c66a2-153">-AccountId</span></span>

<span data-ttu-id="c66a2-154">Konto-ID för åtkomsttoken i **AccessToken** parameter set.</span><span class="sxs-lookup"><span data-stu-id="c66a2-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="c66a2-155">Konto-ID för hanterad tjänst i **ManagedService** parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c66a2-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="c66a2-156">Kan vara ett hanterat tjänst resurs-ID eller associerat klient-ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="c66a2-157">Lämna det här fältet tomt om du vill använda den tilldelade system identiteten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c66a2-158">-ApplicationId</span></span>

<span data-ttu-id="c66a2-159">Program-ID för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="c66a2-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c66a2-160">-CertificateThumbprint</span></span>

<span data-ttu-id="c66a2-161">Certifikat-hash eller tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="c66a2-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="c66a2-162">-ContextName</span></span>

<span data-ttu-id="c66a2-163">Namn på standard kontext för Azure för den här inloggningen.</span><span class="sxs-lookup"><span data-stu-id="c66a2-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="c66a2-164">Mer information om Azure-kontexter finns i avsnittet om [objekt i Azure PowerShell](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="c66a2-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="c66a2-165">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="c66a2-165">-Credential</span></span>

<span data-ttu-id="c66a2-166">Anger ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c66a2-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="c66a2-167">Om du vill ha mer information om **PSCredential** -objektet skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c66a2-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="c66a2-168">**PSCredential** -objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="c66a2-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66a2-169">-DefaultProfile</span></span>

<span data-ttu-id="c66a2-170">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c66a2-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c66a2-171">-Miljö</span><span class="sxs-lookup"><span data-stu-id="c66a2-171">-Environment</span></span>

<span data-ttu-id="c66a2-172">Miljö med Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="c66a2-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-173">-Force</span><span class="sxs-lookup"><span data-stu-id="c66a2-173">-Force</span></span>

<span data-ttu-id="c66a2-174">Skriv över den befintliga kontexten med samma namn utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="c66a2-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="c66a2-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="c66a2-175">-GraphAccessToken</span></span>

<span data-ttu-id="c66a2-176">AccessToken för Graph-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="c66a2-177">-Identity</span></span>

<span data-ttu-id="c66a2-178">Logga in med ett hanterat tjänst-ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="c66a2-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="c66a2-180">AccessToken för valv tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="c66a2-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="c66a2-182">Aktuell.</span><span class="sxs-lookup"><span data-stu-id="c66a2-182">Obsolete.</span></span> <span data-ttu-id="c66a2-183">Om du vill använda en anpassad MSI-slutpunkt måste du ange miljövariabeln MSI_ENDPOINT, till exempel " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="c66a2-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="c66a2-184">Värdnamn för den hanterade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-184">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="c66a2-185">-ManagedServicePort</span></span>

<span data-ttu-id="c66a2-186">Aktuell.</span><span class="sxs-lookup"><span data-stu-id="c66a2-186">Obsolete.</span></span> <span data-ttu-id="c66a2-187">Om du vill använda en anpassad MSI-slutpunkt måste du ange miljövariabeln MSI_ENDPOINT, till exempel " http://localhost:50342/oauth2/token ". Port nummer för den hanterade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="c66a2-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="c66a2-189">Aktuell.</span><span class="sxs-lookup"><span data-stu-id="c66a2-189">Obsolete.</span></span> <span data-ttu-id="c66a2-190">Om du vill använda anpassad MSI-hemlighet måste du ange miljövariabeln MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="c66a2-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="c66a2-191">Token för den hanterade tjänst inloggningen.</span><span class="sxs-lookup"><span data-stu-id="c66a2-191">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c66a2-192">-MaxContextPopulation</span></span>

<span data-ttu-id="c66a2-193">Maximalt abonnemangs nummer för att fylla i kontexter efter inloggning.</span><span class="sxs-lookup"><span data-stu-id="c66a2-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="c66a2-194">Standard är 25.</span><span class="sxs-lookup"><span data-stu-id="c66a2-194">Default is 25.</span></span> <span data-ttu-id="c66a2-195">Om du vill fylla alla abonnemang mot text anger du-1.</span><span class="sxs-lookup"><span data-stu-id="c66a2-195">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-196">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c66a2-196">-Scope</span></span>

<span data-ttu-id="c66a2-197">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="c66a2-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c66a2-198">-ServicePrincipal</span></span>

<span data-ttu-id="c66a2-199">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="c66a2-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="c66a2-200">-SkipContextPopulation</span></span>

<span data-ttu-id="c66a2-201">Hoppar över kontext populationen om ingen kontext hittas.</span><span class="sxs-lookup"><span data-stu-id="c66a2-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="c66a2-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="c66a2-202">-SkipValidation</span></span>

<span data-ttu-id="c66a2-203">Hoppa över verifiering för åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="c66a2-203">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-204">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="c66a2-204">-Subscription</span></span>

<span data-ttu-id="c66a2-205">Prenumerationens namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-205">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-206">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="c66a2-206">-Tenant</span></span>

<span data-ttu-id="c66a2-207">Valfritt klient namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="c66a2-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="c66a2-208">På grund av begränsningar i det aktuella API: t måste du använda ett klient-ID i stället för ett klient organisations namn när du ansluter till ett B2B-konto (Business-to-Business).</span><span class="sxs-lookup"><span data-stu-id="c66a2-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="c66a2-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="c66a2-210">Använd enhets kod i stället för en webb läsar kontroll.</span><span class="sxs-lookup"><span data-stu-id="c66a2-210">Use device code authentication instead of a browser control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66a2-211">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c66a2-211">-Confirm</span></span>

<span data-ttu-id="c66a2-212">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c66a2-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c66a2-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c66a2-213">-WhatIf</span></span>

<span data-ttu-id="c66a2-214">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c66a2-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c66a2-215">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c66a2-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c66a2-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66a2-216">CommonParameters</span></span>
<span data-ttu-id="c66a2-217">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c66a2-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66a2-218">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c66a2-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66a2-219">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c66a2-219">INPUTS</span></span>

### <span data-ttu-id="c66a2-220">System. String</span><span class="sxs-lookup"><span data-stu-id="c66a2-220">System.String</span></span>

## <span data-ttu-id="c66a2-221">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c66a2-221">OUTPUTS</span></span>

### <span data-ttu-id="c66a2-222">Microsoft. Azure. commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c66a2-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="c66a2-223">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c66a2-223">NOTES</span></span>

## <span data-ttu-id="c66a2-224">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c66a2-224">RELATED LINKS</span></span>
