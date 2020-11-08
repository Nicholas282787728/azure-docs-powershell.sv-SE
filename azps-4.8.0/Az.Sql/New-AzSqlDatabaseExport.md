---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: c5b0295458d0efe443dc20ab069ccfb62a44eb49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258543"
---
# <span data-ttu-id="a769d-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="a769d-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="a769d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a769d-102">SYNOPSIS</span></span>
<span data-ttu-id="a769d-103">Exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a769d-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="a769d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a769d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a769d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a769d-105">DESCRIPTION</span></span>
<span data-ttu-id="a769d-106">Cmdleten **New-AzSqlDatabaseExport** exporterar en Azure SQL-databas som en. bacpac-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a769d-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="a769d-107">Status förfrågan för skaffa export databas kan skickas för att hämta statusinformation för denna begäran.</span><span class="sxs-lookup"><span data-stu-id="a769d-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="a769d-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="a769d-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a769d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a769d-109">EXAMPLES</span></span>

### <span data-ttu-id="a769d-110">Exempel 1: skapa en export förfrågan för en databas</span><span class="sxs-lookup"><span data-stu-id="a769d-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="a769d-111">Det här kommandot skapar en export förfrågan för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="a769d-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="a769d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a769d-112">PARAMETERS</span></span>

### <span data-ttu-id="a769d-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="a769d-113">-AdministratorLogin</span></span>
<span data-ttu-id="a769d-114">Anger namnet på SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="a769d-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="a769d-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a769d-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a769d-116">Anger lösen ordet för SQL-administratören.</span><span class="sxs-lookup"><span data-stu-id="a769d-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="a769d-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a769d-117">-AuthenticationType</span></span>
<span data-ttu-id="a769d-118">Anger vilken typ av verifikation som används för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="a769d-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="a769d-119">Standardvärdet är SQL om ingen autentiseringstyp är angiven.</span><span class="sxs-lookup"><span data-stu-id="a769d-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="a769d-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a769d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a769d-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="a769d-121">Sql.</span></span>
<span data-ttu-id="a769d-122">SQL-verifikation.</span><span class="sxs-lookup"><span data-stu-id="a769d-122">SQL authentication.</span></span>
<span data-ttu-id="a769d-123">Ställ in *AdministratorLogin* och *AdministratorLoginPassword* på SQL-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="a769d-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="a769d-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="a769d-124">ADPassword.</span></span>
<span data-ttu-id="a769d-125">Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="a769d-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="a769d-126">Ange *AdministratorLogin* och *ADMINISTRATORLOGINPASSWORD* till Azure AD-administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="a769d-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="a769d-127">Den här parametern är endast tillgänglig på V12-servrar för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="a769d-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="a769d-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a769d-128">-DatabaseName</span></span>
<span data-ttu-id="a769d-129">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a769d-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="a769d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a769d-130">-DefaultProfile</span></span>
<span data-ttu-id="a769d-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a769d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a769d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a769d-132">-ResourceGroupName</span></span>
<span data-ttu-id="a769d-133">Anger namnet på resurs gruppen för SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="a769d-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="a769d-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a769d-134">-ServerName</span></span>
<span data-ttu-id="a769d-135">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="a769d-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="a769d-136">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="a769d-136">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="a769d-137">ID för SQL Server-resurs för att skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="a769d-137">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="a769d-138">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="a769d-138">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="a769d-139">Resurs-ID för lagrings konto för att skapa en privat länk</span><span class="sxs-lookup"><span data-stu-id="a769d-139">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="a769d-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a769d-140">-StorageKey</span></span>
<span data-ttu-id="a769d-141">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a769d-141">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="a769d-142">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a769d-142">-StorageKeyType</span></span>
<span data-ttu-id="a769d-143">Anger typen av åtkomst nycklar för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a769d-143">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="a769d-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a769d-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a769d-145">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a769d-145">StorageAccessKey.</span></span>
<span data-ttu-id="a769d-146">I det här värdet används en lagrings konto profil.</span><span class="sxs-lookup"><span data-stu-id="a769d-146">This value uses a storage account key.</span></span> 
- <span data-ttu-id="a769d-147">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a769d-147">SharedAccessKey.</span></span>
<span data-ttu-id="a769d-148">I det här värdet används en delad åtkomst-signaturnyckel (SAS).</span><span class="sxs-lookup"><span data-stu-id="a769d-148">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="a769d-149">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a769d-149">-StorageUri</span></span>
<span data-ttu-id="a769d-150">Anger BLOB-länken som en URL till. bacpac-filen.</span><span class="sxs-lookup"><span data-stu-id="a769d-150">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="a769d-151">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="a769d-151">-UseNetworkIsolation</span></span>
<span data-ttu-id="a769d-152">Om den anges skapar den privata länken för lagrings konto och/eller SQL Server</span><span class="sxs-lookup"><span data-stu-id="a769d-152">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="a769d-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a769d-153">-Confirm</span></span>
<span data-ttu-id="a769d-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a769d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a769d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a769d-155">-WhatIf</span></span>
<span data-ttu-id="a769d-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a769d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a769d-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a769d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a769d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a769d-158">CommonParameters</span></span>
<span data-ttu-id="a769d-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a769d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a769d-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a769d-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a769d-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a769d-161">INPUTS</span></span>

### <span data-ttu-id="a769d-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a769d-162">System.String</span></span>

## <span data-ttu-id="a769d-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a769d-163">OUTPUTS</span></span>

### <span data-ttu-id="a769d-164">Microsoft. Azure. commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="a769d-164">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="a769d-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a769d-165">NOTES</span></span>
* <span data-ttu-id="a769d-166">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="a769d-166">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a769d-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a769d-167">RELATED LINKS</span></span>

[<span data-ttu-id="a769d-168">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="a769d-168">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="a769d-169">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="a769d-169">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="a769d-170">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a769d-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
