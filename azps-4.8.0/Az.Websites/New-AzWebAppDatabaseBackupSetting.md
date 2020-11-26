---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: d9e8f70908c9e2c9149d22cae59609ff189164d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259737"
---
# <span data-ttu-id="57d68-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="57d68-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="57d68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57d68-102">SYNOPSIS</span></span>

## <span data-ttu-id="57d68-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57d68-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d68-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57d68-104">DESCRIPTION</span></span>
<span data-ttu-id="57d68-105">Cmdleten **New-AzWebAppDatabaseBackupSetting** skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="57d68-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="57d68-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57d68-106">EXAMPLES</span></span>

### <span data-ttu-id="57d68-107">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="57d68-107">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="57d68-108">Skapar en säkerhets kopierings inställning för databasen (anslutnings sträng) av typen SqlAzure för den angivna app-ContosoWebApp i resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="57d68-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="57d68-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="57d68-109">Example 2</span></span>

<span data-ttu-id="57d68-110">New-AzWebAppDatabaseBackupSetting-cmdleten skapar en ny Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="57d68-110">The New-AzWebAppDatabaseBackupSetting cmdlet creates a new Azure Web App Backup setting.</span></span> <span data-ttu-id="57d68-111">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="57d68-111">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppDatabaseBackupSetting -ConnectionString 'MyConnectionString' -ConnectionStringName <String> -DatabaseType 'SqlAzure' -Name 'ContosoWebApp'
```

## <span data-ttu-id="57d68-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57d68-112">PARAMETERS</span></span>

### <span data-ttu-id="57d68-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="57d68-113">-ConnectionString</span></span>
<span data-ttu-id="57d68-114">Anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="57d68-114">Connection String</span></span>

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

### <span data-ttu-id="57d68-115">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="57d68-115">-ConnectionStringName</span></span>
<span data-ttu-id="57d68-116">Namn på anslutnings strängen</span><span class="sxs-lookup"><span data-stu-id="57d68-116">Connection String Name</span></span>

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

### <span data-ttu-id="57d68-117">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="57d68-117">-DatabaseType</span></span>
<span data-ttu-id="57d68-118">Databas typ (till exempel "SqlAzure" eller "MySql")</span><span class="sxs-lookup"><span data-stu-id="57d68-118">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="57d68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d68-119">-DefaultProfile</span></span>
<span data-ttu-id="57d68-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57d68-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57d68-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="57d68-121">-Name</span></span>
<span data-ttu-id="57d68-122">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="57d68-122">WebApp Name</span></span>

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

### <span data-ttu-id="57d68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d68-123">CommonParameters</span></span>
<span data-ttu-id="57d68-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d68-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d68-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d68-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57d68-126">INPUTS</span></span>

### <span data-ttu-id="57d68-127">System. String</span><span class="sxs-lookup"><span data-stu-id="57d68-127">System.String</span></span>

## <span data-ttu-id="57d68-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57d68-128">OUTPUTS</span></span>

### <span data-ttu-id="57d68-129">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="57d68-129">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="57d68-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57d68-130">NOTES</span></span>

## <span data-ttu-id="57d68-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57d68-131">RELATED LINKS</span></span>