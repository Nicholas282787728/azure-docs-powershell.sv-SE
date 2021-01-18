---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522264"
---
# <span data-ttu-id="523b6-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="523b6-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="523b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="523b6-102">SYNOPSIS</span></span>
<span data-ttu-id="523b6-103">Exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="523b6-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="523b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="523b6-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="523b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="523b6-105">DESCRIPTION</span></span>
<span data-ttu-id="523b6-106">Cmdleten **New-AzSqlDatabaseExport** exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="523b6-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="523b6-107">Status förfrågan för skaffa export databas kan skickas för att hämta statusinformation för denna begäran.</span><span class="sxs-lookup"><span data-stu-id="523b6-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="523b6-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="523b6-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="523b6-109">För att du ska kunna använda denna cmdlet måste brand väggen på Azure SQL Server konfigureras till "Tillåt Azure-tjänster och-resurser att få åtkomst till den här servern".</span><span class="sxs-lookup"><span data-stu-id="523b6-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="523b6-110">Om det inte har kon figurer ATS kommer GatewayTimeout-fel att uppstå.</span><span class="sxs-lookup"><span data-stu-id="523b6-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="523b6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="523b6-111">EXAMPLES</span></span>

### <span data-ttu-id="523b6-112">Exempel 1: skapa en export förfrågan för en databas</span><span class="sxs-lookup"><span data-stu-id="523b6-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="523b6-113">Det här kommandot skapar en export förfrågan för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="523b6-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="523b6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="523b6-114">PARAMETERS</span></span>

### <span data-ttu-id="523b6-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="523b6-115">-AdministratorLogin</span></span>
<span data-ttu-id="523b6-116">Anger namnet på SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="523b6-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="523b6-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="523b6-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="523b6-118">Anger lösen ordet för SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="523b6-118">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="523b6-119">-AuthenticationType</span></span>
<span data-ttu-id="523b6-120">Anger vilken typ av verifikation som används för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="523b6-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="523b6-121">Standardvärdet är SQL om ingen autentiseringstyp är angiven.</span><span class="sxs-lookup"><span data-stu-id="523b6-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="523b6-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="523b6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="523b6-123">SQL.</span><span class="sxs-lookup"><span data-stu-id="523b6-123">Sql.</span></span>
<span data-ttu-id="523b6-124">SQL-verifikation.</span><span class="sxs-lookup"><span data-stu-id="523b6-124">SQL authentication.</span></span>
<span data-ttu-id="523b6-125">Ställ in *AdministratorLogin* och *AdministratorLoginPassword* på SQL-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="523b6-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="523b6-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="523b6-126">ADPassword.</span></span>
<span data-ttu-id="523b6-127">Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="523b6-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="523b6-128">Ange *AdministratorLogin* och *ADMINISTRATORLOGINPASSWORD* till Azure AD-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="523b6-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="523b6-129">Den här parametern är endast tillgänglig på V12-servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="523b6-129">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="523b6-130">-DatabaseName</span></span>
<span data-ttu-id="523b6-131">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="523b6-131">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523b6-132">-DefaultProfile</span></span>
<span data-ttu-id="523b6-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="523b6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="523b6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523b6-134">-ResourceGroupName</span></span>
<span data-ttu-id="523b6-135">Anger namnet på resurs gruppen för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="523b6-135">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="523b6-136">-ServerName</span></span>
<span data-ttu-id="523b6-137">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="523b6-137">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="523b6-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="523b6-139">ID för SQL Server-resurs för att skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="523b6-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="523b6-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="523b6-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="523b6-141">Resurs-ID för lagrings konto för att skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="523b6-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="523b6-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="523b6-142">-StorageKey</span></span>
<span data-ttu-id="523b6-143">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="523b6-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="523b6-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="523b6-144">-StorageKeyType</span></span>
<span data-ttu-id="523b6-145">Anger typen av åtkomst nycklar för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="523b6-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="523b6-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="523b6-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="523b6-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="523b6-147">StorageAccessKey.</span></span>
<span data-ttu-id="523b6-148">I det här värdet används en lagrings konto profil.</span><span class="sxs-lookup"><span data-stu-id="523b6-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="523b6-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="523b6-149">SharedAccessKey.</span></span>
<span data-ttu-id="523b6-150">I det här värdet används en delad åtkomst-signaturnyckel (SAS).</span><span class="sxs-lookup"><span data-stu-id="523b6-150">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="523b6-151">-StorageUri</span></span>
<span data-ttu-id="523b6-152">Anger BLOB-länken som en URL till. bacpac-filen.</span><span class="sxs-lookup"><span data-stu-id="523b6-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="523b6-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="523b6-154">Om den anges skapar den privata länken för lagrings konto och/eller SQL Server</span><span class="sxs-lookup"><span data-stu-id="523b6-154">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b6-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="523b6-155">-Confirm</span></span>
<span data-ttu-id="523b6-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="523b6-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523b6-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523b6-157">-WhatIf</span></span>
<span data-ttu-id="523b6-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="523b6-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523b6-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="523b6-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523b6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523b6-160">CommonParameters</span></span>
<span data-ttu-id="523b6-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523b6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523b6-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="523b6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523b6-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="523b6-163">INPUTS</span></span>

### <span data-ttu-id="523b6-164">System. String</span><span class="sxs-lookup"><span data-stu-id="523b6-164">System.String</span></span>

## <span data-ttu-id="523b6-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="523b6-165">OUTPUTS</span></span>

### <span data-ttu-id="523b6-166">Microsoft. Azure. commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="523b6-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="523b6-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="523b6-167">NOTES</span></span>
* <span data-ttu-id="523b6-168">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="523b6-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="523b6-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="523b6-169">RELATED LINKS</span></span>

[<span data-ttu-id="523b6-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="523b6-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="523b6-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="523b6-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="523b6-172">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="523b6-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
