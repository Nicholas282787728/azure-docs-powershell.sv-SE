---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574953"
---
# <span data-ttu-id="e370f-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e370f-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="e370f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e370f-102">SYNOPSIS</span></span>
<span data-ttu-id="e370f-103">Skapar en ny anslutnings information ett objekt som anger Server typ och namn för anslutning.</span><span class="sxs-lookup"><span data-stu-id="e370f-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e370f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e370f-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="e370f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e370f-105">DESCRIPTION</span></span>
<span data-ttu-id="e370f-106">New-AzureRmDataMigrationConnectionInfo cmdlet skapar ny en anslutnings information som anger Server typen för anslutning.</span><span class="sxs-lookup"><span data-stu-id="e370f-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="e370f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e370f-107">EXAMPLES</span></span>

### <span data-ttu-id="e370f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e370f-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="e370f-109">I det föregående exemplet skapas en ny anslutnings information med parametern SQL as ServerType.</span><span class="sxs-lookup"><span data-stu-id="e370f-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="e370f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e370f-110">PARAMETERS</span></span>

### <span data-ttu-id="e370f-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e370f-111">-Confirm</span></span>
<span data-ttu-id="e370f-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e370f-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e370f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e370f-113">-DefaultProfile</span></span>
<span data-ttu-id="e370f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e370f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e370f-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="e370f-115">-ServerType</span></span>
<span data-ttu-id="e370f-116">Fasttext som beskriver Server typen som du vill ansluta till.</span><span class="sxs-lookup"><span data-stu-id="e370f-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="e370f-117">Funktioner som stöds för närvarande är SQL för SQL Server och SQLDB för SQL Azure-databasen.</span><span class="sxs-lookup"><span data-stu-id="e370f-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e370f-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="e370f-118">-AuthType</span></span>
<span data-ttu-id="e370f-119">Autentiseringstyp som ska användas för anslutning.</span><span class="sxs-lookup"><span data-stu-id="e370f-119">Authentication type to use for connection.</span></span> <span data-ttu-id="e370f-120">Möjliga värden är SqlAuthentication och WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e370f-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e370f-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="e370f-121">-DataSource</span></span>
<span data-ttu-id="e370f-122">Server address\name att ansluta till.</span><span class="sxs-lookup"><span data-stu-id="e370f-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e370f-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="e370f-123">-TrustServerCertificate</span></span>
<span data-ttu-id="e370f-124">Booleskt värde som anger att krypteringen sker.</span><span class="sxs-lookup"><span data-stu-id="e370f-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e370f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e370f-125">-WhatIf</span></span>
<span data-ttu-id="e370f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e370f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e370f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e370f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="e370f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e370f-128">INPUTS</span></span>

### <span data-ttu-id="e370f-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="e370f-129">None</span></span>


## <span data-ttu-id="e370f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e370f-130">OUTPUTS</span></span>

### <span data-ttu-id="e370f-131">Microsoft. Azure. Management. DataMigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e370f-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="e370f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e370f-132">NOTES</span></span>

## <span data-ttu-id="e370f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e370f-133">RELATED LINKS</span></span>

