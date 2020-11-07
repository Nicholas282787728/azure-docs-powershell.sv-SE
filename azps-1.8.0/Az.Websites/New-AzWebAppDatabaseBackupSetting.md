---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746053"
---
# <span data-ttu-id="737b7-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="737b7-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="737b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="737b7-102">SYNOPSIS</span></span>

## <span data-ttu-id="737b7-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="737b7-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737b7-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="737b7-104">DESCRIPTION</span></span>
<span data-ttu-id="737b7-105">Cmdleten **New-AzWebAppDatabaseBackupSetting** skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="737b7-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="737b7-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="737b7-106">EXAMPLES</span></span>

### <span data-ttu-id="737b7-107">9.1</span><span class="sxs-lookup"><span data-stu-id="737b7-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="737b7-108">Skapar en säkerhets kopierings inställning för databasen (anslutnings sträng) av typen SqlAzure för den angivna app-ContosoWebApp i resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="737b7-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="737b7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="737b7-109">PARAMETERS</span></span>

### <span data-ttu-id="737b7-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="737b7-110">-ConnectionString</span></span>
<span data-ttu-id="737b7-111">Anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="737b7-111">Connection String</span></span>

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

### <span data-ttu-id="737b7-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="737b7-112">-ConnectionStringName</span></span>
<span data-ttu-id="737b7-113">Namn på anslutnings strängen</span><span class="sxs-lookup"><span data-stu-id="737b7-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737b7-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="737b7-114">-DatabaseType</span></span>
<span data-ttu-id="737b7-115">Databas typ (till exempel "SqlAzure" eller "MySql")</span><span class="sxs-lookup"><span data-stu-id="737b7-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="737b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737b7-116">-DefaultProfile</span></span>
<span data-ttu-id="737b7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="737b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="737b7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="737b7-118">-Name</span></span>
<span data-ttu-id="737b7-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="737b7-119">WebApp Name</span></span>

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

### <span data-ttu-id="737b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737b7-120">CommonParameters</span></span>
<span data-ttu-id="737b7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737b7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737b7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737b7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="737b7-123">INPUTS</span></span>

### <span data-ttu-id="737b7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="737b7-124">System.String</span></span>

## <span data-ttu-id="737b7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="737b7-125">OUTPUTS</span></span>

### <span data-ttu-id="737b7-126">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="737b7-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="737b7-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="737b7-127">NOTES</span></span>

## <span data-ttu-id="737b7-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="737b7-128">RELATED LINKS</span></span>
