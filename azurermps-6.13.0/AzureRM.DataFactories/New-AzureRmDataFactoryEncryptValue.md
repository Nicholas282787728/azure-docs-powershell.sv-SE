---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 5de4c34281b2122880a683f070e771dc15d93c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583576"
---
# <span data-ttu-id="d14c4-101">New-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="d14c4-101">New-AzureRmDataFactoryEncryptValue</span></span>

## <span data-ttu-id="d14c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d14c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d14c4-103">Krypterar känsliga data.</span><span class="sxs-lookup"><span data-stu-id="d14c4-103">Encrypts sensitive data.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d14c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d14c4-104">SYNTAX</span></span>

### <span data-ttu-id="d14c4-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="d14c4-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d14c4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d14c4-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d14c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d14c4-107">DESCRIPTION</span></span>
<span data-ttu-id="d14c4-108">Den **nya** cmdleten AzureRmDataFactoryEncryptValue krypterar känsliga data, till exempel ett lösen ord eller en Microsoft SQL Server-anslutningssträng, och returnerar ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="d14c4-108">The **New-AzureRmDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="d14c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d14c4-109">EXAMPLES</span></span>

### <span data-ttu-id="d14c4-110">Exempel 1: kryptera en icke-ODBC-anslutningssträng</span><span class="sxs-lookup"><span data-stu-id="d14c4-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="d14c4-111">I det första kommandot används ConvertTo-SecureString cmdlet för att konvertera den angivna anslutnings strängen till ett **SecureString** -objekt och sedan lagras objektet i $Value-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d14c4-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="d14c4-112">Om du vill ha mer information skriver du `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="d14c4-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="d14c4-113">Tillåtna värden: SQL Server eller Oracle-anslutningssträng.</span><span class="sxs-lookup"><span data-stu-id="d14c4-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="d14c4-114">Det andra kommandot skapar ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="d14c4-115">Exempel 2: kryptera en icke-ODBC-anslutningssträng som använder Windows-inloggning.</span><span class="sxs-lookup"><span data-stu-id="d14c4-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="d14c4-116">Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna anslutnings strängen till ett säkert String-objekt och lagrar sedan objektet i variabeln $Value.</span><span class="sxs-lookup"><span data-stu-id="d14c4-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="d14c4-117">Det andra kommandot använder cmdleten Get-Credential för att samla in Windows-inloggningen (användar namn och lösen ord) och lagrar sedan **PSCredential** -objektet i $Credential-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d14c4-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="d14c4-118">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d14c4-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="d14c4-119">Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="d14c4-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="d14c4-120">Exempel 3: kryptera Server namn och autentiseringsuppgifter för den länkade tjänsten för fil system</span><span class="sxs-lookup"><span data-stu-id="d14c4-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="d14c4-121">Det första kommandot använder **ConvertTo-SecureString** för att konvertera den angivna strängen till en säker sträng och lagrar sedan objektet i variabeln $Value.</span><span class="sxs-lookup"><span data-stu-id="d14c4-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="d14c4-122">Det andra kommandot används för att samla in Windows-autentisering (användar namn och lösen ord) och lagrar sedan **PSCredential** **-** objektet i variabeln $Credential.</span><span class="sxs-lookup"><span data-stu-id="d14c4-122">The second command uses **Get-Credential** to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="d14c4-123">Det tredje kommandot skapar ett krypterat värde för det objekt som lagras i $Value och $Credential för angiven data fabrik, Gateway, resurs grupp och länkad tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="d14c4-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="d14c4-124">Exempel 4: krypterar autentiseringsuppgifter för den länkade tjänsten HDFS</span><span class="sxs-lookup"><span data-stu-id="d14c4-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="d14c4-125">Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.</span><span class="sxs-lookup"><span data-stu-id="d14c4-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="d14c4-126">Kommandot **ny-objekt** skapar ett PSCredential-objekt med hjälp av de säkra användar-och lösen ords strängarna.</span><span class="sxs-lookup"><span data-stu-id="d14c4-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="d14c4-127">I stället kan du använda kommandot **Hämta-autentiseringsuppgifter** för att samla in Windows-autentisering (användar namn och lösen ord) och sedan lagra det returnerade **PSCredential** -objektet i $Credential variabel enligt föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="d14c4-127">Instead, you could use the **Get-Credential** command to collect windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="d14c4-128">Med kommandot **ny-AzureRmDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Credential för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-128">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="d14c4-129">Exempel 5: krypterings-autentiseringsuppgifter för ODBC-länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="d14c4-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="d14c4-130">Med kommandot **ConvertTo-SecureString** konverteras den angivna strängen till en säker sträng.</span><span class="sxs-lookup"><span data-stu-id="d14c4-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="d14c4-131">Med kommandot **ny-AzureRmDataFactoryEncryptValue** skapas ett krypterat värde för det objekt som lagras i $Value för den angivna data fabriks-, Gateway-, resurs grupp-och länkad tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-131">The **New-AzureRmDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="d14c4-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d14c4-132">PARAMETERS</span></span>

### <span data-ttu-id="d14c4-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d14c4-133">-AuthenticationType</span></span>
<span data-ttu-id="d14c4-134">Anger vilken typ av verifikation som ska användas för att ansluta till data källan.</span><span class="sxs-lookup"><span data-stu-id="d14c4-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="d14c4-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d14c4-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d14c4-136">Windows</span><span class="sxs-lookup"><span data-stu-id="d14c4-136">Windows</span></span>
- <span data-ttu-id="d14c4-137">Basisk</span><span class="sxs-lookup"><span data-stu-id="d14c4-137">Basic</span></span>
- <span data-ttu-id="d14c4-138">Anonym.</span><span class="sxs-lookup"><span data-stu-id="d14c4-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-139">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="d14c4-139">-Credential</span></span>
<span data-ttu-id="d14c4-140">Anger Windows autentiseringsinformation (användar namn och lösen ord) som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d14c4-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="d14c4-141">Denna cmdlet krypterar de autentiseringsuppgifter du anger här.</span><span class="sxs-lookup"><span data-stu-id="d14c4-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-142">-Databas</span><span class="sxs-lookup"><span data-stu-id="d14c4-142">-Database</span></span>
<span data-ttu-id="d14c4-143">Anger databas namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d14c4-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d14c4-144">-DataFactory</span></span>
<span data-ttu-id="d14c4-145">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d14c4-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d14c4-146">Denna cmdlet krypterar data för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d14c4-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d14c4-147">-DataFactoryName</span></span>
<span data-ttu-id="d14c4-148">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d14c4-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d14c4-149">Denna cmdlet krypterar data för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d14c4-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14c4-150">-DefaultProfile</span></span>
<span data-ttu-id="d14c4-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d14c4-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d14c4-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="d14c4-152">-GatewayName</span></span>
<span data-ttu-id="d14c4-153">Anger namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="d14c4-154">Denna cmdlet krypterar data för den gateway som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d14c4-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="d14c4-155">-NonCredentialValue</span></span>
<span data-ttu-id="d14c4-156">Anger icke-Credential-delen av ODBC-anslutningssträng (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="d14c4-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="d14c4-157">Den här parametern används endast för den länkade ODBC-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d14c4-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14c4-158">-ResourceGroupName</span></span>
<span data-ttu-id="d14c4-159">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d14c4-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d14c4-160">Denna cmdlet krypterar data för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d14c4-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-161">-Server</span><span class="sxs-lookup"><span data-stu-id="d14c4-161">-Server</span></span>
<span data-ttu-id="d14c4-162">Anger Server namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d14c4-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-163">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d14c4-163">-Type</span></span>
<span data-ttu-id="d14c4-164">Anger den länkade tjänst typen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-164">Specifies the linked service type.</span></span>
<span data-ttu-id="d14c4-165">Denna cmdlet krypterar data för den länkade tjänst typen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d14c4-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="d14c4-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d14c4-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d14c4-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="d14c4-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="d14c4-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="d14c4-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="d14c4-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="d14c4-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="d14c4-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="d14c4-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="d14c4-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="d14c4-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-176">-Värde</span><span class="sxs-lookup"><span data-stu-id="d14c4-176">-Value</span></span>
<span data-ttu-id="d14c4-177">Anger det värde som ska krypteras.</span><span class="sxs-lookup"><span data-stu-id="d14c4-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="d14c4-178">Använd en anslutnings sträng för en lokal SQL Server-länkad tjänst och en lokal Oracle-länkad tjänst.</span><span class="sxs-lookup"><span data-stu-id="d14c4-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="d14c4-179">För en lokal ODBC-länkad tjänst kan du använda Credential-delen av anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="d14c4-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="d14c4-180">För den länkade tjänsten för lokala fil system, om fil systemet är lokalt för gateway-datorn, Använd lokal eller localhost, och om fil systemet finns på en annan server än gateway-datorn, Använd \\ \\ Server namn.</span><span class="sxs-lookup"><span data-stu-id="d14c4-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d14c4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14c4-181">CommonParameters</span></span>
<span data-ttu-id="d14c4-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14c4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14c4-183">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d14c4-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14c4-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d14c4-184">INPUTS</span></span>

### <span data-ttu-id="d14c4-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d14c4-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d14c4-186">System. String</span><span class="sxs-lookup"><span data-stu-id="d14c4-186">System.String</span></span>

## <span data-ttu-id="d14c4-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d14c4-187">OUTPUTS</span></span>

### <span data-ttu-id="d14c4-188">System. String</span><span class="sxs-lookup"><span data-stu-id="d14c4-188">System.String</span></span>

## <span data-ttu-id="d14c4-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d14c4-189">NOTES</span></span>
* <span data-ttu-id="d14c4-190">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="d14c4-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d14c4-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d14c4-191">RELATED LINKS</span></span>

[<span data-ttu-id="d14c4-192">New-AzureRmDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="d14c4-192">New-AzureRmDataFactoryEncryptValue</span></span>](./New-AzureRmDataFactoryEncryptValue.md)


