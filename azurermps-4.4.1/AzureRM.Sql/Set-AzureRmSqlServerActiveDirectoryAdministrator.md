---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579707"
---
# <span data-ttu-id="ceaa5-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceaa5-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ceaa5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ceaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="ceaa5-103">Etablerar en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceaa5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ceaa5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceaa5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ceaa5-105">DESCRIPTION</span></span>
<span data-ttu-id="ceaa5-106">Cmdleten **set-AzureRmSqlServerActiveDirectoryAdministrator** etablerar en Azure AD-administratör för AzureSQL server i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="ceaa5-107">Du kan endast etablera en administratör åt gången.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="ceaa5-108">Följande medlemmar i Azure AD kan etableras som SQL Server-administratör:</span><span class="sxs-lookup"><span data-stu-id="ceaa5-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="ceaa5-109">Egna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="ceaa5-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="ceaa5-110">Sammanslagna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="ceaa5-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="ceaa5-111">Importerade medlemmar från andra Azure-annonser som är egna eller sammanlänkade medlemmar</span><span class="sxs-lookup"><span data-stu-id="ceaa5-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="ceaa5-112">Azure AD-grupper som har skapats som säkerhets grupper</span><span class="sxs-lookup"><span data-stu-id="ceaa5-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="ceaa5-113">Microsoft-konton, till exempel dem i Outlook.com-, Hotmail.com-eller Live.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="ceaa5-114">Andra gäst konton, till exempel dem i Gmail.com-eller Yahoo.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="ceaa5-115">Vi rekommenderar att du tillhandahåller en dedikerad Azure AD-grupp som administratör.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="ceaa5-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ceaa5-116">EXAMPLES</span></span>

### <span data-ttu-id="ceaa5-117">Exempel 1: etablera en administratörs grupp för en server</span><span class="sxs-lookup"><span data-stu-id="ceaa5-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ceaa5-118">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="ceaa5-119">Den här servern är kopplad till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ceaa5-120">Exempel 2: etablera en administratörs användare för en server</span><span class="sxs-lookup"><span data-stu-id="ceaa5-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="ceaa5-121">Det här kommandot etablerar en Azure AD-användare som administratör för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="ceaa5-122">Exempel 3: etablera en administratörs grupp genom att ange dess ID</span><span class="sxs-lookup"><span data-stu-id="ceaa5-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ceaa5-123">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="ceaa5-124">Kommandot anger ett ID för parametern *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="ceaa5-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="ceaa5-125">Det gör att kommandot fungerar även om gruppens visnings namn inte är unikt.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="ceaa5-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ceaa5-126">PARAMETERS</span></span>

### <span data-ttu-id="ceaa5-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ceaa5-127">-DisplayName</span></span>
<span data-ttu-id="ceaa5-128">Anger visnings namnet på den Azure AD-administratör som denna cmdlet etablerar.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="ceaa5-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ceaa5-129">-ObjectId</span></span>
<span data-ttu-id="ceaa5-130">Anger unikt ID för den Azure AD-administratör som denna cmdlet etablerar.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="ceaa5-131">Om visnings namnet inte är unikt måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaa5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceaa5-132">-ResourceGroupName</span></span>
<span data-ttu-id="ceaa5-133">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ceaa5-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ceaa5-134">-ServerName</span></span>
<span data-ttu-id="ceaa5-135">Anger namnet på den SQL Server där denna cmdlet etablerar en administratör.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="ceaa5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ceaa5-136">-Confirm</span></span>
<span data-ttu-id="ceaa5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceaa5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceaa5-138">-WhatIf</span></span>
<span data-ttu-id="ceaa5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceaa5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceaa5-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceaa5-141">-DefaultProfile</span></span>
<span data-ttu-id="ceaa5-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceaa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceaa5-143">CommonParameters</span></span>
<span data-ttu-id="ceaa5-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceaa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceaa5-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceaa5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceaa5-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ceaa5-146">INPUTS</span></span>

## <span data-ttu-id="ceaa5-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ceaa5-147">OUTPUTS</span></span>

### <span data-ttu-id="ceaa5-148">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ceaa5-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ceaa5-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ceaa5-149">NOTES</span></span>

## <span data-ttu-id="ceaa5-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ceaa5-150">RELATED LINKS</span></span>

[<span data-ttu-id="ceaa5-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceaa5-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ceaa5-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ceaa5-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ceaa5-153">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ceaa5-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


