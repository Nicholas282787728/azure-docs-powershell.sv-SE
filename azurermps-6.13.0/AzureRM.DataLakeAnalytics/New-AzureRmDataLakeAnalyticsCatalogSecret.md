---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582704"
---
# <span data-ttu-id="64dac-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="64dac-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="64dac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64dac-102">SYNOPSIS</span></span>
<span data-ttu-id="64dac-103">Skapar en hemliga katalog hemlighet för data Lake.</span><span class="sxs-lookup"><span data-stu-id="64dac-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64dac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64dac-104">SYNTAX</span></span>

### <span data-ttu-id="64dac-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="64dac-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64dac-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="64dac-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64dac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64dac-107">DESCRIPTION</span></span>
<span data-ttu-id="64dac-108">Cmdleten **New-AzureRmDataLakeAnalyticsCatalogSecret** skapar en hemlighet som kan användas i en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="64dac-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="64dac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64dac-109">EXAMPLES</span></span>

### <span data-ttu-id="64dac-110">Exempel 1: få hemligheten för en katalog</span><span class="sxs-lookup"><span data-stu-id="64dac-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="64dac-111">Det här kommandot får hemligheten som motsvarar det angivna kontot, databasen, autentiseringsuppgiften och värden.</span><span class="sxs-lookup"><span data-stu-id="64dac-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="64dac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64dac-112">PARAMETERS</span></span>

### <span data-ttu-id="64dac-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="64dac-113">-Account</span></span>
<span data-ttu-id="64dac-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="64dac-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="64dac-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="64dac-115">-DatabaseHost</span></span>
<span data-ttu-id="64dac-116">Anger värd namnet på den databas som hemligheten associerats med i formatet ' mydatabase.contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="64dac-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dac-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64dac-117">-DatabaseName</span></span>
<span data-ttu-id="64dac-118">Anger namnet på den databas som innehåller hemligheten.</span><span class="sxs-lookup"><span data-stu-id="64dac-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="64dac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dac-119">-DefaultProfile</span></span>
<span data-ttu-id="64dac-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="64dac-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64dac-121">-Port</span><span class="sxs-lookup"><span data-stu-id="64dac-121">-Port</span></span>
<span data-ttu-id="64dac-122">Anger det hemliga port numret för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="64dac-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dac-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="64dac-123">-Secret</span></span>
<span data-ttu-id="64dac-124">Anger namn och lösen ord för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="64dac-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dac-125">-URI</span><span class="sxs-lookup"><span data-stu-id="64dac-125">-Uri</span></span>
<span data-ttu-id="64dac-126">Anger hemlighetens URI (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="64dac-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dac-127">CommonParameters</span></span>
<span data-ttu-id="64dac-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dac-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dac-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dac-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64dac-130">INPUTS</span></span>

### <span data-ttu-id="64dac-131">System. String</span><span class="sxs-lookup"><span data-stu-id="64dac-131">System.String</span></span>

### <span data-ttu-id="64dac-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="64dac-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="64dac-133">System. URI</span><span class="sxs-lookup"><span data-stu-id="64dac-133">System.Uri</span></span>

### <span data-ttu-id="64dac-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64dac-134">System.Int32</span></span>

## <span data-ttu-id="64dac-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64dac-135">OUTPUTS</span></span>

### <span data-ttu-id="64dac-136">Microsoft. Azure. Management. DataLake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="64dac-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="64dac-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64dac-137">NOTES</span></span>

## <span data-ttu-id="64dac-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64dac-138">RELATED LINKS</span></span>

[<span data-ttu-id="64dac-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="64dac-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="64dac-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="64dac-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


