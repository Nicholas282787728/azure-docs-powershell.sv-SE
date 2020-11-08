---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dd134408f45d1c24f3a40366026ab66a54b8ff41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919126"
---
# <span data-ttu-id="4f6f3-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="4f6f3-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="4f6f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6f3-103">Lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="4f6f3-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="4f6f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f6f3-104">SYNTAX</span></span>

### <span data-ttu-id="4f6f3-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f6f3-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6f3-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f6f3-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6f3-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f6f3-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f6f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f6f3-108">DESCRIPTION</span></span>
<span data-ttu-id="4f6f3-109">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="4f6f3-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="4f6f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="4f6f3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f6f3-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="4f6f3-112">Lägga till TDE-certifikat till en SQL-Server med resurs grupp namn och SQL Server-namn</span><span class="sxs-lookup"><span data-stu-id="4f6f3-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="4f6f3-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4f6f3-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="4f6f3-114">Lägga till TDE-certifikat till servrarna med Server-resourceId</span><span class="sxs-lookup"><span data-stu-id="4f6f3-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="4f6f3-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4f6f3-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="4f6f3-116">Lägga till TDE-certifikat till alla SQL-servrar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="4f6f3-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="4f6f3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f6f3-117">PARAMETERS</span></span>

### <span data-ttu-id="4f6f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6f3-118">-DefaultProfile</span></span>
<span data-ttu-id="4f6f3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f6f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f6f3-120">-PassThru</span></span>
<span data-ttu-id="4f6f3-121">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="4f6f3-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="4f6f3-122">-Password</span></span>
<span data-ttu-id="4f6f3-123">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="4f6f3-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="4f6f3-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="4f6f3-124">-PrivateBlob</span></span>
<span data-ttu-id="4f6f3-125">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="4f6f3-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="4f6f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f6f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f6f3-127">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="4f6f3-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="4f6f3-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f6f3-128">-ServerName</span></span>
<span data-ttu-id="4f6f3-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="4f6f3-129">The Server Name</span></span>

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

### <span data-ttu-id="4f6f3-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="4f6f3-130">-SqlServer</span></span>
<span data-ttu-id="4f6f3-131">SQL Server-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="4f6f3-131">The sql server input object</span></span>

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

### <span data-ttu-id="4f6f3-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="4f6f3-132">-SqlServerResourceId</span></span>
<span data-ttu-id="4f6f3-133">Resurs-ID för SQL Server</span><span class="sxs-lookup"><span data-stu-id="4f6f3-133">The sql server resource id</span></span>

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

### <span data-ttu-id="4f6f3-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f6f3-134">-Confirm</span></span>
<span data-ttu-id="4f6f3-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f6f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f6f3-136">-WhatIf</span></span>
<span data-ttu-id="4f6f3-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f6f3-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f6f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6f3-139">CommonParameters</span></span>
<span data-ttu-id="4f6f3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6f3-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f6f3-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6f3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f6f3-142">INPUTS</span></span>

### <span data-ttu-id="4f6f3-143">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="4f6f3-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4f6f3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4f6f3-144">System.String</span></span>

## <span data-ttu-id="4f6f3-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f6f3-145">OUTPUTS</span></span>

### <span data-ttu-id="4f6f3-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f6f3-146">System.Boolean</span></span>

## <span data-ttu-id="4f6f3-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f6f3-147">NOTES</span></span>

## <span data-ttu-id="4f6f3-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f6f3-148">RELATED LINKS</span></span>