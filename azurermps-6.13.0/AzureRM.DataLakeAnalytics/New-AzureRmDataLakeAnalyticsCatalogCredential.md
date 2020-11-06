---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2d239e8c40c4e2472ee26a2f08b14a8f7871bd80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582707"
---
# <span data-ttu-id="30747-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="30747-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="30747-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30747-102">SYNOPSIS</span></span>
<span data-ttu-id="30747-103">Skapar en ny autentisering för Azure Data Lake-katalog.</span><span class="sxs-lookup"><span data-stu-id="30747-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30747-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30747-104">SYNTAX</span></span>

### <span data-ttu-id="30747-105">CreateByHostNameAndPort (standard)</span><span class="sxs-lookup"><span data-stu-id="30747-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30747-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="30747-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30747-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30747-107">DESCRIPTION</span></span>
<span data-ttu-id="30747-108">New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet skapar en ny autentiseringsuppgift som kan användas i en Azure Data Lake Analytics-katalog för anslutning till externa data källor.</span><span class="sxs-lookup"><span data-stu-id="30747-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="30747-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30747-109">EXAMPLES</span></span>

### <span data-ttu-id="30747-110">Exempel 1: skapa en autentiseringsuppgift för en katalog som anger värd och port</span><span class="sxs-lookup"><span data-stu-id="30747-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="30747-111">Det här kommandot skapar den angivna autentiseringsuppgiften för angivet konto, databas, värd och port via HTTPS-protokollet.</span><span class="sxs-lookup"><span data-stu-id="30747-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="30747-112">Exempel 2: skapa en autentiseringsuppgift för en katalog med fullständig URI</span><span class="sxs-lookup"><span data-stu-id="30747-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="30747-113">Det här kommandot skapar den angivna autentiseringsuppgiften för det angivna kontot, databasen och URI för extern data källa.</span><span class="sxs-lookup"><span data-stu-id="30747-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="30747-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30747-114">PARAMETERS</span></span>

### <span data-ttu-id="30747-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="30747-115">-Account</span></span>
<span data-ttu-id="30747-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="30747-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30747-117">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="30747-117">-Credential</span></span>
<span data-ttu-id="30747-118">Anger användar namn och lösen ord för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="30747-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30747-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="30747-119">-CredentialName</span></span>
<span data-ttu-id="30747-120">Anger namn och lösen ord för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="30747-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="30747-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="30747-121">-DatabaseHost</span></span>
<span data-ttu-id="30747-122">Anger värd namnet på den externa data källan som autentiseringsuppgiften kan ansluta till i formatet mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="30747-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30747-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30747-123">-DatabaseName</span></span>
<span data-ttu-id="30747-124">Anger namnet på den databas i data Lake Analytics-kontot som autentiseringsuppgiften lagras i.</span><span class="sxs-lookup"><span data-stu-id="30747-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="30747-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30747-125">-DefaultProfile</span></span>
<span data-ttu-id="30747-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="30747-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30747-127">-Port</span><span class="sxs-lookup"><span data-stu-id="30747-127">-Port</span></span>
<span data-ttu-id="30747-128">Anger det port nummer som används för att ansluta till angiven DatabaseHost med dessa autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="30747-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30747-129">-URI</span><span class="sxs-lookup"><span data-stu-id="30747-129">-Uri</span></span>
<span data-ttu-id="30747-130">Anger fullständig URI (Uniform Resource Identifier) för den externa data källan som den här autentiseringsuppgiften kan ansluta till.</span><span class="sxs-lookup"><span data-stu-id="30747-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30747-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30747-131">-Confirm</span></span>
<span data-ttu-id="30747-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30747-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30747-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30747-133">-WhatIf</span></span>
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

### <span data-ttu-id="30747-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30747-134">CommonParameters</span></span>
<span data-ttu-id="30747-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30747-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30747-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30747-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30747-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30747-137">INPUTS</span></span>

### <span data-ttu-id="30747-138">System. String</span><span class="sxs-lookup"><span data-stu-id="30747-138">System.String</span></span>

### <span data-ttu-id="30747-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="30747-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="30747-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="30747-140">System.Uri</span></span>

### <span data-ttu-id="30747-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="30747-141">System.Int32</span></span>

## <span data-ttu-id="30747-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30747-142">OUTPUTS</span></span>

### <span data-ttu-id="30747-143">Microsoft. Azure. Management. DataLake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="30747-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="30747-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30747-144">NOTES</span></span>

## <span data-ttu-id="30747-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30747-145">RELATED LINKS</span></span>
