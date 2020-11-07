---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e807d1fd1c630554bbaefe0cae1dd225b5f1a184
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757000"
---
# <span data-ttu-id="de1a2-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="de1a2-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="de1a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="de1a2-103">Ändrar en katalog hemlighet för data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="de1a2-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de1a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de1a2-104">SYNTAX</span></span>

### <span data-ttu-id="de1a2-105">Ange fullständig URI</span><span class="sxs-lookup"><span data-stu-id="de1a2-105">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de1a2-106">Ange värdnamn och port</span><span class="sxs-lookup"><span data-stu-id="de1a2-106">Specify host name and port</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de1a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de1a2-107">DESCRIPTION</span></span>
<span data-ttu-id="de1a2-108">Cmdleten **set-AzureRmDataLakeAnalyticsCatalogSecret** ändrar en hemlighet som är kopplad till en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="de1a2-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="de1a2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de1a2-109">EXAMPLES</span></span>

### <span data-ttu-id="de1a2-110">Exempel 1: ändra hemligheten som associeras med ett konto</span><span class="sxs-lookup"><span data-stu-id="de1a2-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="de1a2-111">Det här kommandot ställer in hemligheten som är kopplad till en data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="de1a2-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="de1a2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de1a2-112">PARAMETERS</span></span>

### <span data-ttu-id="de1a2-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="de1a2-113">-Account</span></span>
<span data-ttu-id="de1a2-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="de1a2-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="de1a2-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="de1a2-115">-DatabaseHost</span></span>
<span data-ttu-id="de1a2-116">Anger värd namnet på den databas som hemligheten associerats med i formatet ' mydatabase.contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="de1a2-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de1a2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de1a2-117">-DatabaseName</span></span>
<span data-ttu-id="de1a2-118">Anger namnet på den databas som innehåller hemligheten.</span><span class="sxs-lookup"><span data-stu-id="de1a2-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="de1a2-119">-Port</span><span class="sxs-lookup"><span data-stu-id="de1a2-119">-Port</span></span>
<span data-ttu-id="de1a2-120">Anger det hemliga port numret för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="de1a2-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de1a2-121">-Secret</span><span class="sxs-lookup"><span data-stu-id="de1a2-121">-Secret</span></span>
<span data-ttu-id="de1a2-122">Anger namn och lösen ord för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="de1a2-122">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="de1a2-123">-URI</span><span class="sxs-lookup"><span data-stu-id="de1a2-123">-Uri</span></span>
<span data-ttu-id="de1a2-124">Anger URI (Uniform Resource Identifier) för hemligheten.</span><span class="sxs-lookup"><span data-stu-id="de1a2-124">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de1a2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1a2-125">-DefaultProfile</span></span>
<span data-ttu-id="de1a2-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de1a2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de1a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1a2-127">CommonParameters</span></span>
<span data-ttu-id="de1a2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1a2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1a2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de1a2-130">INPUTS</span></span>

## <span data-ttu-id="de1a2-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de1a2-131">OUTPUTS</span></span>

### <span data-ttu-id="de1a2-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="de1a2-132">None</span></span>

## <span data-ttu-id="de1a2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de1a2-133">NOTES</span></span>

## <span data-ttu-id="de1a2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de1a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="de1a2-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="de1a2-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="de1a2-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="de1a2-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


