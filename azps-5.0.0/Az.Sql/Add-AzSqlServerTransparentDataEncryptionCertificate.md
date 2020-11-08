---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262930"
---
# <span data-ttu-id="db7f4-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="db7f4-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="db7f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="db7f4-103">Lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="db7f4-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="db7f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db7f4-104">SYNTAX</span></span>

### <span data-ttu-id="db7f4-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db7f4-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7f4-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db7f4-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7f4-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db7f4-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db7f4-108">DESCRIPTION</span></span>
<span data-ttu-id="db7f4-109">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="db7f4-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="db7f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db7f4-110">EXAMPLES</span></span>

### <span data-ttu-id="db7f4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db7f4-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="db7f4-112">Lägga till TDE-certifikat till en SQL-Server med resurs grupp namn och SQL Server-namn</span><span class="sxs-lookup"><span data-stu-id="db7f4-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="db7f4-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="db7f4-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="db7f4-114">Lägga till TDE-certifikat till servrarna med Server-resourceId</span><span class="sxs-lookup"><span data-stu-id="db7f4-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="db7f4-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="db7f4-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="db7f4-116">Lägga till TDE-certifikat till alla SQL-servrar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="db7f4-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="db7f4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db7f4-117">PARAMETERS</span></span>

### <span data-ttu-id="db7f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7f4-118">-DefaultProfile</span></span>
<span data-ttu-id="db7f4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db7f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db7f4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db7f4-120">-PassThru</span></span>
<span data-ttu-id="db7f4-121">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="db7f4-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="db7f4-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="db7f4-122">-Password</span></span>
<span data-ttu-id="db7f4-123">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="db7f4-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="db7f4-124">-PrivateBlob</span></span>
<span data-ttu-id="db7f4-125">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="db7f4-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db7f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="db7f4-127">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="db7f4-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db7f4-128">-ServerName</span></span>
<span data-ttu-id="db7f4-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="db7f4-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="db7f4-130">-SqlServer</span></span>
<span data-ttu-id="db7f4-131">SQL Server-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="db7f4-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="db7f4-132">-SqlServerResourceId</span></span>
<span data-ttu-id="db7f4-133">Resurs-ID för SQL Server</span><span class="sxs-lookup"><span data-stu-id="db7f4-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db7f4-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db7f4-134">-Confirm</span></span>
<span data-ttu-id="db7f4-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db7f4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7f4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7f4-136">-WhatIf</span></span>
<span data-ttu-id="db7f4-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db7f4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db7f4-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db7f4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7f4-139">CommonParameters</span></span>
<span data-ttu-id="db7f4-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db7f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7f4-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db7f4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7f4-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db7f4-142">INPUTS</span></span>

### <span data-ttu-id="db7f4-143">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="db7f4-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="db7f4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="db7f4-144">System.String</span></span>

## <span data-ttu-id="db7f4-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db7f4-145">OUTPUTS</span></span>

### <span data-ttu-id="db7f4-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db7f4-146">System.Boolean</span></span>

## <span data-ttu-id="db7f4-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db7f4-147">NOTES</span></span>

## <span data-ttu-id="db7f4-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db7f4-148">RELATED LINKS</span></span>
