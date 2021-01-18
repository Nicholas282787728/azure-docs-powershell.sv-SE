---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520231"
---
# <span data-ttu-id="e4ac1-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e4ac1-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e4ac1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ac1-103">Skapar en ny autentisering för Azure Data Lake-katalog.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="e4ac1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4ac1-104">SYNTAX</span></span>

### <span data-ttu-id="e4ac1-105">CreateByHostNameAndPort (standard)</span><span class="sxs-lookup"><span data-stu-id="e4ac1-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ac1-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="e4ac1-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ac1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="e4ac1-108">New-AzDataLakeAnalyticsCatalogCredential cmdlet skapar en ny autentiseringsuppgift som kan användas i en Azure Data Lake Analytics-katalog för anslutning till externa data källor.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="e4ac1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="e4ac1-110">Exempel 1: skapa en autentiseringsuppgift för en katalog som anger värd och port</span><span class="sxs-lookup"><span data-stu-id="e4ac1-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="e4ac1-111">Det här kommandot skapar den angivna autentiseringsuppgiften för angivet konto, databas, värd och port via HTTPS-protokollet.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="e4ac1-112">Exempel 2: skapa en autentiseringsuppgift för en katalog med fullständig URI</span><span class="sxs-lookup"><span data-stu-id="e4ac1-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="e4ac1-113">Det här kommandot skapar den angivna autentiseringsuppgiften för det angivna kontot, databasen och URI för extern data källa.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="e4ac1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4ac1-114">PARAMETERS</span></span>

### <span data-ttu-id="e4ac1-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="e4ac1-115">-Account</span></span>
<span data-ttu-id="e4ac1-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e4ac1-117">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="e4ac1-117">-Credential</span></span>
<span data-ttu-id="e4ac1-118">Anger användar namn och lösen ord för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="e4ac1-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e4ac1-119">-CredentialName</span></span>
<span data-ttu-id="e4ac1-120">Anger namn och lösen ord för autentiseringsuppgifterna.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="e4ac1-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e4ac1-121">-DatabaseHost</span></span>
<span data-ttu-id="e4ac1-122">Anger värd namnet på den externa data källan som autentiseringsuppgiften kan ansluta till i formatet mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="e4ac1-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4ac1-123">-DatabaseName</span></span>
<span data-ttu-id="e4ac1-124">Anger namnet på den databas i data Lake Analytics-kontot som autentiseringsuppgiften lagras i.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="e4ac1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ac1-125">-DefaultProfile</span></span>
<span data-ttu-id="e4ac1-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e4ac1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4ac1-127">-Port</span><span class="sxs-lookup"><span data-stu-id="e4ac1-127">-Port</span></span>
<span data-ttu-id="e4ac1-128">Anger det port nummer som används för att ansluta till angiven DatabaseHost med dessa autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="e4ac1-129">-URI</span><span class="sxs-lookup"><span data-stu-id="e4ac1-129">-Uri</span></span>
<span data-ttu-id="e4ac1-130">Anger fullständig URI (Uniform Resource Identifier) för den externa data källan som den här autentiseringsuppgiften kan ansluta till.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="e4ac1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4ac1-131">-Confirm</span></span>
<span data-ttu-id="e4ac1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ac1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ac1-133">-WhatIf</span></span>
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

### <span data-ttu-id="e4ac1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ac1-134">CommonParameters</span></span>
<span data-ttu-id="e4ac1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ac1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ac1-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ac1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ac1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4ac1-137">INPUTS</span></span>

### <span data-ttu-id="e4ac1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e4ac1-138">System.String</span></span>

### <span data-ttu-id="e4ac1-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e4ac1-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e4ac1-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="e4ac1-140">System.Uri</span></span>

### <span data-ttu-id="e4ac1-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e4ac1-141">System.Int32</span></span>

## <span data-ttu-id="e4ac1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4ac1-142">OUTPUTS</span></span>

### <span data-ttu-id="e4ac1-143">Microsoft. Azure. Management. DataLake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="e4ac1-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="e4ac1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4ac1-144">NOTES</span></span>

## <span data-ttu-id="e4ac1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4ac1-145">RELATED LINKS</span></span>
