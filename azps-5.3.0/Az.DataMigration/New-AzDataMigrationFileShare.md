---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426536"
---
# <span data-ttu-id="db401-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="db401-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="db401-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db401-102">SYNOPSIS</span></span>
<span data-ttu-id="db401-103">Skapar FileShare-objektet för Azure Database migration-tjänsten, som anger den lokala nätverks resursen som käll databasens säkerhets kopior ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="db401-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="db401-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db401-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db401-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db401-105">DESCRIPTION</span></span>
<span data-ttu-id="db401-106">New-AzDataMigrationFileShare-cmdleten skapar ett FileShare-objekt som anger den lokala nätverks delning som Azure Database migration-tjänsten kan använda för att säkerhetskopiera käll databasen.</span><span class="sxs-lookup"><span data-stu-id="db401-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="db401-107">Tjänst kontot med SQL Server-instansen för källa måste ha skrivrättigheter för den här nätverks resursen.</span><span class="sxs-lookup"><span data-stu-id="db401-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="db401-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db401-108">EXAMPLES</span></span>

### <span data-ttu-id="db401-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db401-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="db401-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db401-110">PARAMETERS</span></span>

### <span data-ttu-id="db401-111">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="db401-111">-Credential</span></span>
<span data-ttu-id="db401-112">Autentiseringsuppgifter för åtkomst till fil resursen.</span><span class="sxs-lookup"><span data-stu-id="db401-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db401-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db401-113">-DefaultProfile</span></span>
<span data-ttu-id="db401-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db401-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db401-115">-Path</span><span class="sxs-lookup"><span data-stu-id="db401-115">-Path</span></span>
<span data-ttu-id="db401-116">Sökväg till fil resurs.</span><span class="sxs-lookup"><span data-stu-id="db401-116">File share path.</span></span>

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

### <span data-ttu-id="db401-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db401-117">CommonParameters</span></span>
<span data-ttu-id="db401-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db401-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db401-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db401-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db401-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db401-120">INPUTS</span></span>

### <span data-ttu-id="db401-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="db401-121">None</span></span>

## <span data-ttu-id="db401-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db401-122">OUTPUTS</span></span>

### <span data-ttu-id="db401-123">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="db401-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="db401-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db401-124">NOTES</span></span>

## <span data-ttu-id="db401-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db401-125">RELATED LINKS</span></span>
