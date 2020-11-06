---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 333de53ccd3632188100af7f3fcde10e140537c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579972"
---
# <span data-ttu-id="76580-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="76580-101">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="76580-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76580-102">SYNOPSIS</span></span>
<span data-ttu-id="76580-103">Lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="76580-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76580-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76580-104">SYNTAX</span></span>

### <span data-ttu-id="76580-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="76580-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76580-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76580-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76580-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76580-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzureRmSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76580-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76580-108">DESCRIPTION</span></span>
<span data-ttu-id="76580-109">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna SQL Server-instansen</span><span class="sxs-lookup"><span data-stu-id="76580-109">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="76580-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76580-110">EXAMPLES</span></span>

### <span data-ttu-id="76580-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76580-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="76580-112">Lägga till TDE-certifikat till en SQL-Server med resurs grupp namn och SQL Server-namn</span><span class="sxs-lookup"><span data-stu-id="76580-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="76580-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="76580-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzureRmSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzureRmSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="76580-114">Lägga till TDE-certifikat till servrarna med Server-resourceId</span><span class="sxs-lookup"><span data-stu-id="76580-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="76580-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="76580-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzureRmSqlServer | Add-AzureRmSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="76580-116">Lägga till TDE-certifikat till alla SQL-servrar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="76580-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="76580-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76580-117">PARAMETERS</span></span>

### <span data-ttu-id="76580-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76580-118">-DefaultProfile</span></span>
<span data-ttu-id="76580-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76580-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76580-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76580-120">-PassThru</span></span>
<span data-ttu-id="76580-121">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="76580-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="76580-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="76580-122">-Password</span></span>
<span data-ttu-id="76580-123">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="76580-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="76580-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="76580-124">-PrivateBlob</span></span>
<span data-ttu-id="76580-125">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="76580-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="76580-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76580-126">-ResourceGroupName</span></span>
<span data-ttu-id="76580-127">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="76580-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="76580-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76580-128">-ServerName</span></span>
<span data-ttu-id="76580-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="76580-129">The Server Name</span></span>

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

### <span data-ttu-id="76580-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="76580-130">-SqlServer</span></span>
<span data-ttu-id="76580-131">SQL Server-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="76580-131">The sql server input object</span></span>

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

### <span data-ttu-id="76580-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="76580-132">-SqlServerResourceId</span></span>
<span data-ttu-id="76580-133">Resurs-ID för SQL Server</span><span class="sxs-lookup"><span data-stu-id="76580-133">The sql server resource id</span></span>

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

### <span data-ttu-id="76580-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76580-134">-Confirm</span></span>
<span data-ttu-id="76580-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76580-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76580-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76580-136">-WhatIf</span></span>
<span data-ttu-id="76580-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76580-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76580-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76580-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76580-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76580-139">CommonParameters</span></span>
<span data-ttu-id="76580-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76580-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76580-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76580-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76580-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76580-142">INPUTS</span></span>

### <span data-ttu-id="76580-143">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="76580-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="76580-144">Parametrar: SqlServer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76580-144">Parameters: SqlServer (ByValue)</span></span>

### <span data-ttu-id="76580-145">System. String</span><span class="sxs-lookup"><span data-stu-id="76580-145">System.String</span></span>

## <span data-ttu-id="76580-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76580-146">OUTPUTS</span></span>

### <span data-ttu-id="76580-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76580-147">System.Boolean</span></span>

## <span data-ttu-id="76580-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76580-148">NOTES</span></span>

## <span data-ttu-id="76580-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76580-149">RELATED LINKS</span></span>
