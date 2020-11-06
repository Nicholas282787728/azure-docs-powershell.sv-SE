---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 22a10d4f65d43f4d11871cbf43399bfc35febf04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583544"
---
# <span data-ttu-id="e17de-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e17de-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="e17de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e17de-102">SYNOPSIS</span></span>
<span data-ttu-id="e17de-103">Ändrar en katalog hemlighet för data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e17de-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e17de-104">SYNTAX</span></span>

### <span data-ttu-id="e17de-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="e17de-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e17de-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="e17de-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e17de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e17de-107">DESCRIPTION</span></span>
<span data-ttu-id="e17de-108">Cmdleten **set-AzureRmDataLakeAnalyticsCatalogSecret** ändrar en hemlighet som är kopplad till en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="e17de-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e17de-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e17de-109">EXAMPLES</span></span>

### <span data-ttu-id="e17de-110">Exempel 1: ändra hemligheten som associeras med ett konto</span><span class="sxs-lookup"><span data-stu-id="e17de-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="e17de-111">Det här kommandot ställer in hemligheten som är kopplad till en data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="e17de-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="e17de-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e17de-112">PARAMETERS</span></span>

### <span data-ttu-id="e17de-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="e17de-113">-Account</span></span>
<span data-ttu-id="e17de-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e17de-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e17de-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e17de-115">-DatabaseHost</span></span>
<span data-ttu-id="e17de-116">Anger värd namnet på den databas som hemligheten associerats med i formatet ' mydatabase.contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="e17de-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17de-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e17de-117">-DatabaseName</span></span>
<span data-ttu-id="e17de-118">Anger namnet på den databas som innehåller hemligheten.</span><span class="sxs-lookup"><span data-stu-id="e17de-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="e17de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17de-119">-DefaultProfile</span></span>
<span data-ttu-id="e17de-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e17de-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e17de-121">-Port</span><span class="sxs-lookup"><span data-stu-id="e17de-121">-Port</span></span>
<span data-ttu-id="e17de-122">Anger det hemliga port numret för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="e17de-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullUri
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17de-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="e17de-123">-Secret</span></span>
<span data-ttu-id="e17de-124">Anger namn och lösen ord för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="e17de-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="e17de-125">-URI</span><span class="sxs-lookup"><span data-stu-id="e17de-125">-Uri</span></span>
<span data-ttu-id="e17de-126">Anger URI (Uniform Resource Identifier) för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="e17de-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17de-127">CommonParameters</span></span>
<span data-ttu-id="e17de-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17de-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17de-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e17de-130">INPUTS</span></span>

### <span data-ttu-id="e17de-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e17de-131">System.String</span></span>

### <span data-ttu-id="e17de-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e17de-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e17de-133">System. URI</span><span class="sxs-lookup"><span data-stu-id="e17de-133">System.Uri</span></span>

### <span data-ttu-id="e17de-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e17de-134">System.Int32</span></span>

## <span data-ttu-id="e17de-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e17de-135">OUTPUTS</span></span>

### <span data-ttu-id="e17de-136">Microsoft. Azure. Management. DataLake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="e17de-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="e17de-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e17de-137">NOTES</span></span>

## <span data-ttu-id="e17de-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e17de-138">RELATED LINKS</span></span>

[<span data-ttu-id="e17de-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e17de-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="e17de-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e17de-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


