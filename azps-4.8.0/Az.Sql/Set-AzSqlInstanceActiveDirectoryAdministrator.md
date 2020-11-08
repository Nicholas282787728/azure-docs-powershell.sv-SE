---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259019"
---
# <span data-ttu-id="fba87-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="fba87-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="fba87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fba87-102">SYNOPSIS</span></span>
<span data-ttu-id="fba87-103">Etablerar en Azure AD-administratör för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="fba87-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="fba87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fba87-104">SYNTAX</span></span>

### <span data-ttu-id="fba87-105">UseResourceGroupAndInstanceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fba87-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba87-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba87-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fba87-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba87-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fba87-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fba87-108">DESCRIPTION</span></span>
<span data-ttu-id="fba87-109">Cmdleten **set-AzSqlInstanceActiveDirectoryAdministrator** etablerar en Azure AD-administratör för AzureSQL-hanterad instans i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fba87-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="fba87-110">Du kan endast etablera en administratör åt gången.</span><span class="sxs-lookup"><span data-stu-id="fba87-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="fba87-111">Följande medlemmar i Azure AD kan etableras som en SQL-hanterad instans administratör:</span><span class="sxs-lookup"><span data-stu-id="fba87-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="fba87-112">Egna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="fba87-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="fba87-113">Sammanslagna medlemmar i Azure AD</span><span class="sxs-lookup"><span data-stu-id="fba87-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="fba87-114">Azure AD-grupper som skapats som säkerhets grupper importerade medlemmar från andra Azure-annonser stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="fba87-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="fba87-115">Microsoft-konton, till exempel dem i Outlook.com-, Hotmail.com-eller Live.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="fba87-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="fba87-116">Andra gäst konton, till exempel dem i Gmail.com-eller Yahoo.com-domänerna, stöds inte som administratörer.</span><span class="sxs-lookup"><span data-stu-id="fba87-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="fba87-117">Vi rekommenderar att du tillhandahåller en dedikerad Azure AD-grupp som administratör.</span><span class="sxs-lookup"><span data-stu-id="fba87-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="fba87-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fba87-118">EXAMPLES</span></span>

### <span data-ttu-id="fba87-119">Exempel 1: etablera en administratörs grupp för en hanterad instans som är associerad med resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fba87-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="fba87-120">Det här kommandot etablerar en Azure AD-administratörs grupp med namnet DBAs för den hanterade instans som heter ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="fba87-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="fba87-121">Den här servern är kopplad till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fba87-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="fba87-122">Exempel 2: etablera en administratörs användare med hanterat instans objekt</span><span class="sxs-lookup"><span data-stu-id="fba87-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="fba87-123">Det här kommandot etablerar en Azure AD-användare som administratör från den hanterade instans-objekt.</span><span class="sxs-lookup"><span data-stu-id="fba87-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="fba87-124">Exempel 3: etablera en administratör med resurs-ID för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="fba87-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="fba87-125">Det här kommandot etablerar en Azure AD-användare som administratör med resurs-ID för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="fba87-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="fba87-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fba87-126">PARAMETERS</span></span>

### <span data-ttu-id="fba87-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba87-127">-DefaultProfile</span></span>
<span data-ttu-id="fba87-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fba87-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba87-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fba87-129">-DisplayName</span></span>
<span data-ttu-id="fba87-130">Anger visnings namnet på den användare eller grupp som du vill bevilja behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="fba87-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="fba87-131">Visnings namnet måste finnas i den Active Directory som är kopplad till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fba87-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="fba87-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fba87-132">-InputObject</span></span>
<span data-ttu-id="fba87-133">Det hanterade instans objekt som ska användas.</span><span class="sxs-lookup"><span data-stu-id="fba87-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba87-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fba87-134">-InstanceName</span></span>
<span data-ttu-id="fba87-135">SQL-hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="fba87-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba87-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fba87-136">-ObjectId</span></span>
<span data-ttu-id="fba87-137">Anger objekt-ID: t för den användare eller grupp i Azure Active Directory som du vill bevilja behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="fba87-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba87-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba87-138">-ResourceGroupName</span></span>
<span data-ttu-id="fba87-139">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fba87-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba87-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba87-140">-ResourceId</span></span>
<span data-ttu-id="fba87-141">ID för den instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="fba87-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba87-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fba87-142">-Confirm</span></span>
<span data-ttu-id="fba87-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fba87-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba87-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba87-144">-WhatIf</span></span>
<span data-ttu-id="fba87-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fba87-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fba87-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fba87-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba87-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba87-147">CommonParameters</span></span>
<span data-ttu-id="fba87-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba87-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba87-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fba87-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba87-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fba87-150">INPUTS</span></span>

### <span data-ttu-id="fba87-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fba87-151">System.String</span></span>

### <span data-ttu-id="fba87-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fba87-152">System.Guid</span></span>

## <span data-ttu-id="fba87-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fba87-153">OUTPUTS</span></span>

### <span data-ttu-id="fba87-154">Microsoft. Azure. commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="fba87-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="fba87-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fba87-155">NOTES</span></span>

## <span data-ttu-id="fba87-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fba87-156">RELATED LINKS</span></span>

[<span data-ttu-id="fba87-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="fba87-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="fba87-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="fba87-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
