---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088459"
---
# <span data-ttu-id="39c4c-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="39c4c-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="39c4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39c4c-102">SYNOPSIS</span></span>

## <span data-ttu-id="39c4c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39c4c-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39c4c-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39c4c-104">DESCRIPTION</span></span>
<span data-ttu-id="39c4c-105">Cmdleten **New-AzWebAppDatabaseBackupSetting** skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="39c4c-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="39c4c-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39c4c-106">EXAMPLES</span></span>

### <span data-ttu-id="39c4c-107">9.1</span><span class="sxs-lookup"><span data-stu-id="39c4c-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="39c4c-108">Skapar en säkerhets kopierings inställning för databasen (anslutnings sträng) av typen SqlAzure för den angivna app-ContosoWebApp i resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="39c4c-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="39c4c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39c4c-109">PARAMETERS</span></span>

### <span data-ttu-id="39c4c-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="39c4c-110">-ConnectionString</span></span>
<span data-ttu-id="39c4c-111">Anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="39c4c-111">Connection String</span></span>

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

### <span data-ttu-id="39c4c-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="39c4c-112">-ConnectionStringName</span></span>
<span data-ttu-id="39c4c-113">Namn på anslutnings strängen</span><span class="sxs-lookup"><span data-stu-id="39c4c-113">Connection String Name</span></span>

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

### <span data-ttu-id="39c4c-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="39c4c-114">-DatabaseType</span></span>
<span data-ttu-id="39c4c-115">Databas typ (till exempel "SqlAzure" eller "MySql")</span><span class="sxs-lookup"><span data-stu-id="39c4c-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="39c4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c4c-116">-DefaultProfile</span></span>
<span data-ttu-id="39c4c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39c4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c4c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="39c4c-118">-Name</span></span>
<span data-ttu-id="39c4c-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="39c4c-119">WebApp Name</span></span>

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

### <span data-ttu-id="39c4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c4c-120">CommonParameters</span></span>
<span data-ttu-id="39c4c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c4c-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c4c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c4c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39c4c-123">INPUTS</span></span>

### <span data-ttu-id="39c4c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="39c4c-124">System.String</span></span>

## <span data-ttu-id="39c4c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39c4c-125">OUTPUTS</span></span>

### <span data-ttu-id="39c4c-126">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="39c4c-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="39c4c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39c4c-127">NOTES</span></span>

## <span data-ttu-id="39c4c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39c4c-128">RELATED LINKS</span></span>
