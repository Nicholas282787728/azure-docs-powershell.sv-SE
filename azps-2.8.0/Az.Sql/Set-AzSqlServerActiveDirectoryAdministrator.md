---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 44339cb39396b18660d17bdbad0e597ded30ad18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920437"
---
# <span data-ttu-id="a3be3-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a3be3-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a3be3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3be3-102">SYNOPSIS</span></span>
<span data-ttu-id="a3be3-103">Etablerar en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a3be3-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a3be3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3be3-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3be3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3be3-105">DESCRIPTION</span></span>
<span data-ttu-id="a3be3-106">Cmdleten **set-AzSqlServerActiveDirectoryAdministrator** etablerar en Azure AD-administratör för AzureSQL server i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a3be3-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="a3be3-107">Du kan endast etablera en administratör åt gången.</span><span class="sxs-lookup"><span data-stu-id="a3be3-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="a3be3-108">Följande medlemmar i Azure AD kan etableras som SQL Server-administratör:</span><span class="sxs-lookup"><span data-stu-id="a3be3-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="a3be3-109">Egna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="a3be3-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="a3be3-110">Sammanslagna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="a3be3-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="a3be3-111">Importerade medlemmar från andra Azure-annonser som är egna eller sammanlänkade medlemmar</span><span class="sxs-lookup"><span data-stu-id="a3be3-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="a3be3-112">Azure AD-grupper som har skapats som säkerhets grupper Microsoft-konton, till exempel dem i Outlook.com-, Hotmail.com-eller Live.com-domäner, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="a3be3-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a3be3-113">Andra gäst konton, till exempel dem i Gmail.com-eller Yahoo.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="a3be3-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a3be3-114">Vi rekommenderar att du tillhandahåller en dedikerad Azure AD-grupp som administratör.</span><span class="sxs-lookup"><span data-stu-id="a3be3-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="a3be3-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3be3-115">EXAMPLES</span></span>

### <span data-ttu-id="a3be3-116">Exempel 1: etablera en administratörs grupp för en server</span><span class="sxs-lookup"><span data-stu-id="a3be3-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a3be3-117">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="a3be3-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a3be3-118">Den här servern är kopplad till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a3be3-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a3be3-119">Exempel 2: etablera en administratörs användare för en server</span><span class="sxs-lookup"><span data-stu-id="a3be3-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="a3be3-120">Det här kommandot etablerar en Azure AD-användare som administratör för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="a3be3-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="a3be3-121">Exempel 3: etablera en administratörs grupp genom att ange dess ID</span><span class="sxs-lookup"><span data-stu-id="a3be3-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a3be3-122">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="a3be3-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a3be3-123">Kommandot anger ett ID för parametern *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="a3be3-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="a3be3-124">Det gör att kommandot fungerar även om gruppens visnings namn inte är unikt.</span><span class="sxs-lookup"><span data-stu-id="a3be3-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="a3be3-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3be3-125">PARAMETERS</span></span>

### <span data-ttu-id="a3be3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3be3-126">-DefaultProfile</span></span>
<span data-ttu-id="a3be3-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3be3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3be3-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3be3-128">-DisplayName</span></span>
<span data-ttu-id="a3be3-129">Anger visnings namnet på den Azure AD-administratör som denna cmdlet etablerar.</span><span class="sxs-lookup"><span data-stu-id="a3be3-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="a3be3-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a3be3-130">-ObjectId</span></span>
<span data-ttu-id="a3be3-131">Anger unikt ID för den Azure AD-administratör som denna cmdlet etablerar.</span><span class="sxs-lookup"><span data-stu-id="a3be3-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="a3be3-132">Om visnings namnet inte är unikt måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="a3be3-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="a3be3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3be3-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3be3-134">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="a3be3-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a3be3-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3be3-135">-ServerName</span></span>
<span data-ttu-id="a3be3-136">Anger namnet på den SQL Server där denna cmdlet etablerar en administratör.</span><span class="sxs-lookup"><span data-stu-id="a3be3-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="a3be3-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3be3-137">-Confirm</span></span>
<span data-ttu-id="a3be3-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3be3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3be3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3be3-139">-WhatIf</span></span>
<span data-ttu-id="a3be3-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3be3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3be3-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3be3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3be3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3be3-142">CommonParameters</span></span>
<span data-ttu-id="a3be3-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3be3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3be3-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3be3-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3be3-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3be3-145">INPUTS</span></span>

### <span data-ttu-id="a3be3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a3be3-146">System.String</span></span>

### <span data-ttu-id="a3be3-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a3be3-147">System.Guid</span></span>

## <span data-ttu-id="a3be3-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3be3-148">OUTPUTS</span></span>

### <span data-ttu-id="a3be3-149">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a3be3-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a3be3-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3be3-150">NOTES</span></span>

## <span data-ttu-id="a3be3-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3be3-151">RELATED LINKS</span></span>

[<span data-ttu-id="a3be3-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a3be3-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a3be3-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a3be3-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a3be3-154">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a3be3-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


