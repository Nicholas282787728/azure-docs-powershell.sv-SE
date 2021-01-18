---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520999"
---
# <span data-ttu-id="2a748-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2a748-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="2a748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a748-102">SYNOPSIS</span></span>
<span data-ttu-id="2a748-103">Skapar en ny Azure NetApp-fil (ANF) Active Directory-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2a748-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="2a748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a748-104">SYNTAX</span></span>

### <span data-ttu-id="2a748-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2a748-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a748-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a748-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a748-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a748-107">DESCRIPTION</span></span>
<span data-ttu-id="2a748-108">Cmdleten **New-AzNetAppFilesActiveDirectory** skapar en ny Active Directory-konfiguration för ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="2a748-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="2a748-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a748-109">EXAMPLES</span></span>

### <span data-ttu-id="2a748-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a748-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="2a748-111">Det här kommandot får AD-lösenordet från Promt till en secreates den nya Active Directory-konfigurationen för ANF-kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="2a748-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="2a748-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a748-112">PARAMETERS</span></span>

### <span data-ttu-id="2a748-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a748-113">-AccountName</span></span>
<span data-ttu-id="2a748-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="2a748-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2a748-115">-AccountObject</span></span>
<span data-ttu-id="2a748-116">Kontot för den nya säkerhets kopierings principens objekt</span><span class="sxs-lookup"><span data-stu-id="2a748-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="2a748-117">-AdName</span></span>
<span data-ttu-id="2a748-118">Namn på Active Directory-datorn.</span><span class="sxs-lookup"><span data-stu-id="2a748-118">Name of the active directory machine.</span></span>
<span data-ttu-id="2a748-119">Denna valfria parameter används endast när du skapar Kerberos-volymen</span><span class="sxs-lookup"><span data-stu-id="2a748-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="2a748-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="2a748-120">-BackupOperator</span></span>
<span data-ttu-id="2a748-121">Användare som ska läggas till i den inbyggda ansvarig för säkerhets kopiering Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2a748-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="2a748-122">En lista med unika användar namn utan domän specifikation</span><span class="sxs-lookup"><span data-stu-id="2a748-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a748-123">-DefaultProfile</span></span>
<span data-ttu-id="2a748-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a748-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a748-125">-DNS</span><span class="sxs-lookup"><span data-stu-id="2a748-125">-Dns</span></span>
<span data-ttu-id="2a748-126">Kommaavgränsad lista med IP-adresser för DNS-servrar (endast IPv4) för Active Directory-domänen</span><span class="sxs-lookup"><span data-stu-id="2a748-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="2a748-127">-Domain</span></span>
<span data-ttu-id="2a748-128">Namnet på Active Directory-domänen</span><span class="sxs-lookup"><span data-stu-id="2a748-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="2a748-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="2a748-129">-KdcIP</span></span>
<span data-ttu-id="2a748-130">IP-adresser för KDC-servrar för Active Directory-datorn.</span><span class="sxs-lookup"><span data-stu-id="2a748-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="2a748-131">Denna valfria parameter används bara när du skapar Kerberos-volymen.</span><span class="sxs-lookup"><span data-stu-id="2a748-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="2a748-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="2a748-132">-OrganizationalUnit</span></span>
<span data-ttu-id="2a748-133">Organisationsenheten (OU) i Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a748-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="2a748-134">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="2a748-134">-Password</span></span>
<span data-ttu-id="2a748-135">Vanligt text lösen ord för Active Directory Domain Administrator är värdet maskerat i svaret</span><span class="sxs-lookup"><span data-stu-id="2a748-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a748-136">-ResourceGroupName</span></span>
<span data-ttu-id="2a748-137">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="2a748-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="2a748-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="2a748-139">Om LDAP via SSL/TLS är aktiverat måste LDAP-klienten ha Base64-kodat Active Directory-certifikat tjänstens självsignerade rot certifikat UTFÄRDAre, denna valfria parameter används endast för Dual Protocol med LDAP-mappning av volymer.</span><span class="sxs-lookup"><span data-stu-id="2a748-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="2a748-140">-Site</span><span class="sxs-lookup"><span data-stu-id="2a748-140">-Site</span></span>
<span data-ttu-id="2a748-141">Den Active Directory-plats som tjänsten begränsar identifiering av domänkontrollant till</span><span class="sxs-lookup"><span data-stu-id="2a748-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="2a748-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="2a748-142">-SmbServerName</span></span>
<span data-ttu-id="2a748-143">NetBIOS-namnet på SMB-servern.</span><span class="sxs-lookup"><span data-stu-id="2a748-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="2a748-144">Det här namnet registreras som ett dator konto i ANNONSen och används för montering av volymer</span><span class="sxs-lookup"><span data-stu-id="2a748-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="2a748-145">-Username</span><span class="sxs-lookup"><span data-stu-id="2a748-145">-Username</span></span>
<span data-ttu-id="2a748-146">Användar namn för Active Directory-domän administratör</span><span class="sxs-lookup"><span data-stu-id="2a748-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="2a748-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a748-147">-Confirm</span></span>
<span data-ttu-id="2a748-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a748-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a748-149">-WhatIf</span></span>
<span data-ttu-id="2a748-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a748-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a748-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a748-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a748-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a748-152">CommonParameters</span></span>
<span data-ttu-id="2a748-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a748-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a748-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a748-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a748-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a748-155">INPUTS</span></span>

### <span data-ttu-id="2a748-156">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2a748-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2a748-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a748-157">OUTPUTS</span></span>

### <span data-ttu-id="2a748-158">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="2a748-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="2a748-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a748-159">NOTES</span></span>

## <span data-ttu-id="2a748-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a748-160">RELATED LINKS</span></span>
