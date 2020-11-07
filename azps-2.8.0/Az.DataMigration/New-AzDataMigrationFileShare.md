---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: cc09f7ac0a5f4378c65700cd9681118200d629ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744500"
---
# <span data-ttu-id="e9050-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="e9050-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="e9050-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9050-102">SYNOPSIS</span></span>
<span data-ttu-id="e9050-103">Skapar FileShare-objektet för Azure Database migration-tjänsten, som anger den lokala nätverks resursen som käll databasens säkerhets kopior ska skapas för.</span><span class="sxs-lookup"><span data-stu-id="e9050-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="e9050-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9050-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9050-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9050-105">DESCRIPTION</span></span>
<span data-ttu-id="e9050-106">New-AzDataMigrationFileShare-cmdleten skapar ett FileShare-objekt som anger den lokala nätverks delning som Azure Database migration-tjänsten kan använda för att säkerhetskopiera käll databasen.</span><span class="sxs-lookup"><span data-stu-id="e9050-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="e9050-107">Tjänst kontot med SQL Server-instansen för källa måste ha skrivrättigheter för den här nätverks resursen.</span><span class="sxs-lookup"><span data-stu-id="e9050-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="e9050-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9050-108">EXAMPLES</span></span>

### <span data-ttu-id="e9050-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9050-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="e9050-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9050-110">PARAMETERS</span></span>

### <span data-ttu-id="e9050-111">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="e9050-111">-Credential</span></span>
<span data-ttu-id="e9050-112">Autentiseringsuppgifter för åtkomst till fil resursen.</span><span class="sxs-lookup"><span data-stu-id="e9050-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="e9050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9050-113">-DefaultProfile</span></span>
<span data-ttu-id="e9050-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9050-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e9050-115">-Path</span></span>
<span data-ttu-id="e9050-116">Sökväg till fil resurs.</span><span class="sxs-lookup"><span data-stu-id="e9050-116">File share path.</span></span>

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

### <span data-ttu-id="e9050-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9050-117">CommonParameters</span></span>
<span data-ttu-id="e9050-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9050-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9050-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9050-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9050-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9050-120">INPUTS</span></span>

### <span data-ttu-id="e9050-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9050-121">None</span></span>

## <span data-ttu-id="e9050-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9050-122">OUTPUTS</span></span>

### <span data-ttu-id="e9050-123">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="e9050-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="e9050-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9050-124">NOTES</span></span>

## <span data-ttu-id="e9050-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9050-125">RELATED LINKS</span></span>
