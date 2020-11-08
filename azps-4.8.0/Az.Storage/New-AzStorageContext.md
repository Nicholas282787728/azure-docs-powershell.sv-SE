---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258502"
---
# <span data-ttu-id="5a3db-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a3db-101">New-AzStorageContext</span></span>

## <span data-ttu-id="5a3db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a3db-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3db-103">Skapar en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="5a3db-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="5a3db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a3db-104">SYNTAX</span></span>

### <span data-ttu-id="5a3db-105">OAuthAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="5a3db-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a3db-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="5a3db-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a3db-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="5a3db-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="5a3db-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="5a3db-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a3db-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="5a3db-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5a3db-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="5a3db-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a3db-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="5a3db-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5a3db-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="5a3db-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="5a3db-113">Sträng</span><span class="sxs-lookup"><span data-stu-id="5a3db-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="5a3db-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="5a3db-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="5a3db-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a3db-115">DESCRIPTION</span></span>
<span data-ttu-id="5a3db-116">Cmdleten **New-AzStorageContext** skapar en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="5a3db-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="5a3db-117">Standardautentiseringen för en lagrings kontext är OAuth (Azure AD), om det bara finns namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5a3db-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="5a3db-118">Se informationen om lagrings tjänsten i https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .</span><span class="sxs-lookup"><span data-stu-id="5a3db-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="5a3db-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a3db-119">EXAMPLES</span></span>

### <span data-ttu-id="5a3db-120">Exempel 1: skapa en kontext genom att ange ett lagrings konto namn och en nycklar</span><span class="sxs-lookup"><span data-stu-id="5a3db-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="5a3db-121">Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="5a3db-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5a3db-122">Exempel 2: skapa en kontext genom att ange en anslutnings sträng</span><span class="sxs-lookup"><span data-stu-id="5a3db-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="5a3db-123">Det här kommandot skapar en kontext baserat på den angivna anslutnings strängen för kontot ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="5a3db-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="5a3db-124">Exempel 3: skapa en kontext för ett anonymt lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5a3db-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="5a3db-125">Det här kommandot skapar en kontext för anonym användning för kontot med namnet ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="5a3db-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="5a3db-126">Kommandot anger HTTP som ett anslutnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="5a3db-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="5a3db-127">Exempel 4: skapa en kontext med hjälp av det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="5a3db-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="5a3db-128">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5a3db-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="5a3db-129">Kommandot anger den *lokala* parametern.</span><span class="sxs-lookup"><span data-stu-id="5a3db-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="5a3db-130">Exempel 5: Hämta behållaren för det lokala utvecklings lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="5a3db-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="5a3db-131">Det här kommandot skapar en kontext med hjälp av det lokala utvecklings arkivet och skickar sedan den nya kontexten till cmdleten **Get-AzStorageContainer** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="5a3db-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a3db-132">Kommandot hämtar Azure Storage-behållaren för det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5a3db-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="5a3db-133">Exempel 6: Hämta flera behållare</span><span class="sxs-lookup"><span data-stu-id="5a3db-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="5a3db-134">Det första kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot och lagrar sedan kontexten i variabeln $Context 01.</span><span class="sxs-lookup"><span data-stu-id="5a3db-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="5a3db-135">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan kontexten i $Context 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="5a3db-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="5a3db-136">Med kommandot slut får du behållare för de kontexter som lagras i $Context 01 och $Context 02 genom att använda **Get-AzStorageContainer**.</span><span class="sxs-lookup"><span data-stu-id="5a3db-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="5a3db-137">Exempel 7: skapa en kontext med en slut punkt</span><span class="sxs-lookup"><span data-stu-id="5a3db-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="5a3db-138">Det här kommandot skapar en Azure Storage-kontext som har den angivna lagrings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="5a3db-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="5a3db-139">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="5a3db-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5a3db-140">Exempel 8: skapa en kontext med en angiven miljö</span><span class="sxs-lookup"><span data-stu-id="5a3db-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="5a3db-141">Det här kommandot skapar en Azure-lagringsenhet med den angivna Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="5a3db-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="5a3db-142">Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.</span><span class="sxs-lookup"><span data-stu-id="5a3db-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5a3db-143">Exempel 9: skapa en kontext med hjälp av en SAS-token</span><span class="sxs-lookup"><span data-stu-id="5a3db-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="5a3db-144">Det första kommandot skapar en SAS-token med hjälp av cmdleten **New-AzStorageContainerSASToken** för behållaren med namnet ContosoMain och lagrar sedan denna token i $SasToken variabel.</span><span class="sxs-lookup"><span data-stu-id="5a3db-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="5a3db-145">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="5a3db-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="5a3db-146">Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder SAS-token som lagras i $SasToken och lagrar sedan kontexten i $Context-variabeln.</span><span class="sxs-lookup"><span data-stu-id="5a3db-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="5a3db-147">Med kommandot slut visas alla blobbar som är kopplade till behållaren med namnet ContosoMain med hjälp av kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="5a3db-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="5a3db-148">Exempel 10: skapa en kontext med OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="5a3db-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="5a3db-149">Det här kommandot skapar en kontext med Azure AD-autentisering.</span><span class="sxs-lookup"><span data-stu-id="5a3db-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="5a3db-150">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a3db-150">PARAMETERS</span></span>

### <span data-ttu-id="5a3db-151">-Anonym</span><span class="sxs-lookup"><span data-stu-id="5a3db-151">-Anonymous</span></span>
<span data-ttu-id="5a3db-152">Anger att den här cmdleten skapar en Azure-lagringsenhet för anonym inloggning.</span><span class="sxs-lookup"><span data-stu-id="5a3db-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="5a3db-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5a3db-153">-ConnectionString</span></span>
<span data-ttu-id="5a3db-154">Anger en anslutnings sträng för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="5a3db-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="5a3db-155">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="5a3db-155">-Endpoint</span></span>
<span data-ttu-id="5a3db-156">Anger slut punkten för Azure-lagringsplatsen.</span><span class="sxs-lookup"><span data-stu-id="5a3db-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="5a3db-157">-Miljö</span><span class="sxs-lookup"><span data-stu-id="5a3db-157">-Environment</span></span>
<span data-ttu-id="5a3db-158">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="5a3db-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="5a3db-159">De acceptabla värdena för den här parametern är: AzureCloud och AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="5a3db-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="5a3db-160">Om du vill ha mer information skriver du `Get-Help Get-AzEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="5a3db-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="5a3db-161">-Lokal</span><span class="sxs-lookup"><span data-stu-id="5a3db-161">-Local</span></span>
<span data-ttu-id="5a3db-162">Anger att denna cmdlet skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5a3db-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="5a3db-163">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5a3db-163">-Protocol</span></span>
<span data-ttu-id="5a3db-164">Transfer Protocol (https/http).</span><span class="sxs-lookup"><span data-stu-id="5a3db-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="5a3db-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="5a3db-165">-SasToken</span></span>
<span data-ttu-id="5a3db-166">Anger ett SAS-token (Shared Access signatur) för kontexten.</span><span class="sxs-lookup"><span data-stu-id="5a3db-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="5a3db-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a3db-167">-StorageAccountKey</span></span>
<span data-ttu-id="5a3db-168">Anger en Key för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="5a3db-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="5a3db-169">Denna cmdlet skapar en kontext för den parameter som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="5a3db-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a3db-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a3db-170">-StorageAccountName</span></span>
<span data-ttu-id="5a3db-171">Anger ett namn på en Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="5a3db-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="5a3db-172">Denna cmdlet skapar en kontext för det konto som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a3db-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a3db-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="5a3db-173">-UseConnectedAccount</span></span>
<span data-ttu-id="5a3db-174">Anger att den här cmdleten skapar en Azure-lagringsenhet med OAuth-autentisering (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5a3db-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="5a3db-175">En OAuth-autentisering används som standard i cmdlet när ingen annan autentisering har angetts.</span><span class="sxs-lookup"><span data-stu-id="5a3db-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a3db-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3db-176">CommonParameters</span></span>
<span data-ttu-id="5a3db-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a3db-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3db-178">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a3db-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3db-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a3db-179">INPUTS</span></span>

### <span data-ttu-id="5a3db-180">System. String</span><span class="sxs-lookup"><span data-stu-id="5a3db-180">System.String</span></span>

## <span data-ttu-id="5a3db-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a3db-181">OUTPUTS</span></span>

### <span data-ttu-id="5a3db-182">Microsoft. WindowsAzure. commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a3db-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="5a3db-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a3db-183">NOTES</span></span>

## <span data-ttu-id="5a3db-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a3db-184">RELATED LINKS</span></span>

[<span data-ttu-id="5a3db-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5a3db-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="5a3db-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5a3db-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


