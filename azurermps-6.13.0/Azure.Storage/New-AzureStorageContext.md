---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579211"
---
# <span data-ttu-id="3f009-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f009-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="3f009-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f009-102">SYNOPSIS</span></span>
<span data-ttu-id="3f009-103">Skapar en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3f009-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f009-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f009-104">SYNTAX</span></span>

### <span data-ttu-id="3f009-105">OAuthAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="3f009-105">OAuthAccount (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f009-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="3f009-106">AccountNameAndKey</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f009-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f009-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="3f009-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="3f009-108">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f009-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f009-109">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="3f009-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="3f009-110">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f009-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f009-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="3f009-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f009-112">OAuthAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="3f009-113">Sträng</span><span class="sxs-lookup"><span data-stu-id="3f009-113">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="3f009-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="3f009-114">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="3f009-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f009-115">DESCRIPTION</span></span>
<span data-ttu-id="3f009-116">Cmdleten **New-AzureStorageContext** skapar en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="3f009-116">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="3f009-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f009-117">EXAMPLES</span></span>

### <span data-ttu-id="3f009-118">Exempel 1: skapa en kontext genom att ange ett lagrings konto namn och en nycklar</span><span class="sxs-lookup"><span data-stu-id="3f009-118">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="3f009-119">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="3f009-119">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="3f009-120">Exempel 2: skapa en kontext genom att ange en anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="3f009-120">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="3f009-121">Det här kommandot skapar en kontext baserat på den angivna anslutnings strängen för kontot ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="3f009-121">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="3f009-122">Exempel 3: skapa en kontext för ett anonymt lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3f009-122">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="3f009-123">Det här kommandot skapar en kontext för anonym användning för kontot med namnet ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="3f009-123">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="3f009-124">Kommandot anger HTTP som ett anslutnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="3f009-124">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="3f009-125">Exempel 4: skapa en kontext med hjälp av det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="3f009-125">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="3f009-126">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3f009-126">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="3f009-127">Kommandot anger den *lokala* parametern.</span><span class="sxs-lookup"><span data-stu-id="3f009-127">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="3f009-128">Exempel 5: Hämta behållaren för det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="3f009-128">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="3f009-129">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings arkivet och skickar sedan den nya kontexten till cmdleten **Get-AzureStorageContainer** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3f009-129">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3f009-130">Kommandot hämtar Azure Storage-behållaren för det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3f009-130">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="3f009-131">Exempel 6: Hämta flera behållare</span><span class="sxs-lookup"><span data-stu-id="3f009-131">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="3f009-132">Det första kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot och lagrar sedan kontexten i variabeln $Context 01.</span><span class="sxs-lookup"><span data-stu-id="3f009-132">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="3f009-133">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan kontexten i $Context 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3f009-133">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="3f009-134">Med kommandot slut får du behållare för de kontexter som lagras i $Context 01 och $Context 02 genom att använda **Get-AzureStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="3f009-134">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="3f009-135">Exempel 7: skapa en kontext med en slut punkt</span><span class="sxs-lookup"><span data-stu-id="3f009-135">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="3f009-136">Det här kommandot skapar en Azure Storage-kontext som har den angivna lagrings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="3f009-136">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="3f009-137">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="3f009-137">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="3f009-138">Exempel 8: skapa en kontext med en angiven miljö</span><span class="sxs-lookup"><span data-stu-id="3f009-138">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="3f009-139">Det här kommandot skapar en Azure-lagringsenhet med den angivna Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="3f009-139">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="3f009-140">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="3f009-140">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="3f009-141">Exempel 9: skapa en kontext med hjälp av en SAS-token</span><span class="sxs-lookup"><span data-stu-id="3f009-141">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="3f009-142">Det första kommandot skapar en SAS-token med hjälp av cmdleten **New-AzureStorageContainerSASToken** för behållaren med namnet ContosoMain och lagrar sedan denna token i $SasToken variabel.</span><span class="sxs-lookup"><span data-stu-id="3f009-142">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="3f009-143">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="3f009-143">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="3f009-144">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder SAS-token som lagras i $SasToken och lagrar sedan kontexten i $Context-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3f009-144">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="3f009-145">Med kommandot slut visas alla blobbar som är kopplade till behållaren med namnet ContosoMain med hjälp av kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="3f009-145">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="3f009-146">Exempel 10: skapa en kontext med OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="3f009-146">Example 10: Create a context by using the OAuth Authentication</span></span>
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="3f009-147">Det här kommandot skapar en kontext med OAuth-autentisering.</span><span class="sxs-lookup"><span data-stu-id="3f009-147">This command creates a context by using the OAuth Authentication.</span></span>

## <span data-ttu-id="3f009-148">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f009-148">PARAMETERS</span></span>

### <span data-ttu-id="3f009-149">-Anonym</span><span class="sxs-lookup"><span data-stu-id="3f009-149">-Anonymous</span></span>
<span data-ttu-id="3f009-150">Anger att den här cmdleten skapar en Azure-lagringsenhet för anonym inloggning.</span><span class="sxs-lookup"><span data-stu-id="3f009-150">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-151">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3f009-151">-ConnectionString</span></span>
<span data-ttu-id="3f009-152">Anger en anslutnings sträng för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="3f009-152">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-153">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="3f009-153">-Endpoint</span></span>
<span data-ttu-id="3f009-154">Anger slut punkten för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="3f009-154">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-155">-Miljö</span><span class="sxs-lookup"><span data-stu-id="3f009-155">-Environment</span></span>
<span data-ttu-id="3f009-156">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="3f009-156">Specifies the Azure environment.</span></span>
<span data-ttu-id="3f009-157">De acceptabla värdena för den här parametern är: AzureCloud och AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="3f009-157">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="3f009-158">Om du vill ha mer information skriver du `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="3f009-158">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-159">-Lokal</span><span class="sxs-lookup"><span data-stu-id="3f009-159">-Local</span></span>
<span data-ttu-id="3f009-160">Anger att denna cmdlet skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3f009-160">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-161">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3f009-161">-Protocol</span></span>
<span data-ttu-id="3f009-162">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="3f009-162">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-163">-SasToken</span><span class="sxs-lookup"><span data-stu-id="3f009-163">-SasToken</span></span>
<span data-ttu-id="3f009-164">Anger ett SAS-token (Shared Access signatur) för kontexten.</span><span class="sxs-lookup"><span data-stu-id="3f009-164">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-165">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f009-165">-StorageAccountKey</span></span>
<span data-ttu-id="3f009-166">Anger en Key för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="3f009-166">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="3f009-167">Denna cmdlet skapar en kontext för den parameter som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="3f009-167">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-168">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3f009-168">-StorageAccountName</span></span>
<span data-ttu-id="3f009-169">Anger ett namn på en Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3f009-169">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="3f009-170">Denna cmdlet skapar en kontext för det konto som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3f009-170">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-171">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="3f009-171">-UseConnectedAccount</span></span>
<span data-ttu-id="3f009-172">Anger att denna cmdlet skapar en Azure-lagringsenhet med OAuth-autentisering.</span><span class="sxs-lookup"><span data-stu-id="3f009-172">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="3f009-173">En OAuth-autentisering används som standard i cmdleten om du inte har angett någon annan anthentication.</span><span class="sxs-lookup"><span data-stu-id="3f009-173">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-174">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="3f009-174">-UseConnectedAccount</span></span>
<span data-ttu-id="3f009-175">Anger att denna cmdlet skapar en Azure-lagringsenhet med OAuth-autentisering.</span><span class="sxs-lookup"><span data-stu-id="3f009-175">Indicates that this cmdlet creates an Azure Storage context with OAuth Authentication.</span></span>
<span data-ttu-id="3f009-176">En OAuth-autentisering används som standard i cmdleten om du inte har angett någon annan anthentication.</span><span class="sxs-lookup"><span data-stu-id="3f009-176">The cmdlet will use OAuth Authentication by default, when other anthentication not specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f009-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f009-177">CommonParameters</span></span>
<span data-ttu-id="3f009-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f009-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f009-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f009-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f009-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f009-180">INPUTS</span></span>

### <span data-ttu-id="3f009-181">System. String</span><span class="sxs-lookup"><span data-stu-id="3f009-181">System.String</span></span>

## <span data-ttu-id="3f009-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f009-182">OUTPUTS</span></span>

### <span data-ttu-id="3f009-183">Microsoft. WindowsAzure. commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f009-183">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="3f009-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f009-184">NOTES</span></span>

## <span data-ttu-id="3f009-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f009-185">RELATED LINKS</span></span>

[<span data-ttu-id="3f009-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3f009-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="3f009-187">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3f009-187">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


