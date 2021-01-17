---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394667"
---
# <span data-ttu-id="232ab-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="232ab-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="232ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="232ab-102">SYNOPSIS</span></span>
<span data-ttu-id="232ab-103">Uppdaterar en Azure NetApp (ANF) Active Directory-konfiguration till valfri modifiering som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="232ab-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="232ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="232ab-104">SYNTAX</span></span>

### <span data-ttu-id="232ab-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="232ab-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="232ab-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232ab-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="232ab-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="232ab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="232ab-108">DESCRIPTION</span></span>
<span data-ttu-id="232ab-109">Cmdleten **Update-AzNetAppFilesAccount** ändrar en ANF Active Directory-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="232ab-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="232ab-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="232ab-110">EXAMPLES</span></span>

### <span data-ttu-id="232ab-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="232ab-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="232ab-112">Det här kommandot utför en uppdatering av angiven Active Directory-konfiguration och ändrar det användar namn som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="232ab-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="232ab-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="232ab-113">PARAMETERS</span></span>

### <span data-ttu-id="232ab-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="232ab-114">-AccountName</span></span>
<span data-ttu-id="232ab-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="232ab-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="232ab-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="232ab-116">-AccountObject</span></span>
<span data-ttu-id="232ab-117">Kontot för Active Directory-objektet</span><span class="sxs-lookup"><span data-stu-id="232ab-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="232ab-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="232ab-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="232ab-119">ID för Active Directory-ANF</span><span class="sxs-lookup"><span data-stu-id="232ab-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232ab-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="232ab-120">-AdName</span></span>
<span data-ttu-id="232ab-121">Namn på Active Directory-datorn.</span><span class="sxs-lookup"><span data-stu-id="232ab-121">Name of the active directory machine.</span></span>
<span data-ttu-id="232ab-122">Denna valfria parameter används endast när du skapar Kerberos-volymen</span><span class="sxs-lookup"><span data-stu-id="232ab-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="232ab-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="232ab-123">-BackupOperator</span></span>
<span data-ttu-id="232ab-124">Användare som ska läggas till i den inbyggda ansvarig för säkerhets kopiering Active Directory.</span><span class="sxs-lookup"><span data-stu-id="232ab-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="232ab-125">En lista med unika användar namn utan domän specifikation</span><span class="sxs-lookup"><span data-stu-id="232ab-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="232ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232ab-126">-DefaultProfile</span></span>
<span data-ttu-id="232ab-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="232ab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="232ab-128">-DNS</span><span class="sxs-lookup"><span data-stu-id="232ab-128">-Dns</span></span>
<span data-ttu-id="232ab-129">Kommaavgränsad lista med IP-adresser för DNS-servrar (endast IPv4) för Active Directory-domänen</span><span class="sxs-lookup"><span data-stu-id="232ab-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="232ab-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="232ab-130">-Domain</span></span>
<span data-ttu-id="232ab-131">Namnet på Active Directory-domänen</span><span class="sxs-lookup"><span data-stu-id="232ab-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="232ab-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="232ab-132">-InputObject</span></span>
<span data-ttu-id="232ab-133">Active Directory-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="232ab-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232ab-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="232ab-134">-KdcIP</span></span>
<span data-ttu-id="232ab-135">IP-adresser för KDC-servrar för Active Directory-datorn.</span><span class="sxs-lookup"><span data-stu-id="232ab-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="232ab-136">Denna valfria parameter används bara när du skapar Kerberos-volymen.</span><span class="sxs-lookup"><span data-stu-id="232ab-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="232ab-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="232ab-137">-OrganizationalUnit</span></span>
<span data-ttu-id="232ab-138">Organisationsenheten (OU) i Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="232ab-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="232ab-139">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="232ab-139">-Password</span></span>
<span data-ttu-id="232ab-140">Vanligt text lösen ord för Active Directory Domain Administrator är värdet maskerat i svaret</span><span class="sxs-lookup"><span data-stu-id="232ab-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="232ab-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232ab-141">-ResourceGroupName</span></span>
<span data-ttu-id="232ab-142">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="232ab-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="232ab-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="232ab-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="232ab-144">Om LDAP via SSL/TLS är aktiverat måste LDAP-klienten ha Base64-kodat Active Directory-certifikat tjänstens självsignerade rot certifikat UTFÄRDAre, denna valfria parameter används endast för Dual Protocol med LDAP-mappning av volymer.</span><span class="sxs-lookup"><span data-stu-id="232ab-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="232ab-145">-Site</span><span class="sxs-lookup"><span data-stu-id="232ab-145">-Site</span></span>
<span data-ttu-id="232ab-146">Den Active Directory-plats som tjänsten begränsar identifiering av domänkontrollant till</span><span class="sxs-lookup"><span data-stu-id="232ab-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="232ab-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="232ab-147">-SmbServerName</span></span>
<span data-ttu-id="232ab-148">NetBIOS-namnet på SMB-servern.</span><span class="sxs-lookup"><span data-stu-id="232ab-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="232ab-149">Det här namnet registreras som ett dator konto i ANNONSen och används för montering av volymer</span><span class="sxs-lookup"><span data-stu-id="232ab-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="232ab-150">-Username</span><span class="sxs-lookup"><span data-stu-id="232ab-150">-Username</span></span>
<span data-ttu-id="232ab-151">Användar namn för Active Directory-domän administratör</span><span class="sxs-lookup"><span data-stu-id="232ab-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="232ab-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="232ab-152">-Confirm</span></span>
<span data-ttu-id="232ab-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="232ab-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232ab-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232ab-154">-WhatIf</span></span>
<span data-ttu-id="232ab-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="232ab-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232ab-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="232ab-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232ab-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232ab-157">CommonParameters</span></span>
<span data-ttu-id="232ab-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232ab-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232ab-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="232ab-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232ab-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="232ab-160">INPUTS</span></span>

### <span data-ttu-id="232ab-161">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="232ab-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="232ab-162">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="232ab-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="232ab-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="232ab-163">OUTPUTS</span></span>

### <span data-ttu-id="232ab-164">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="232ab-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="232ab-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="232ab-165">NOTES</span></span>

## <span data-ttu-id="232ab-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="232ab-166">RELATED LINKS</span></span>
